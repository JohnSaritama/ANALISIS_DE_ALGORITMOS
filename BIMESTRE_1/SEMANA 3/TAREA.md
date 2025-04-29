CODIGO EN JAVA:

public class MergeSortHelper {
    public static void merge(int[] A, int p, int q, int r) {
        int nL = q - p + 1; // length of A[p..q]
        int nR = r - q;     // length of A[q+1..r]

        // Create temporary arrays
        int[] L = new int[nL];
        int[] R = new int[nR];

        // Copy A[p..q] into L[0..nL-1]
        for (int i = 0; i < nL; i++) {
            L[i] = A[p + i];
        }

        // Copy A[q+1..r] into R[0..nR-1]
        for (int j = 0; j < nR; j++) {
            R[j] = A[q + 1 + j];
        }

        int i = 0; // index for L
        int j = 0; // index for R
        int k = p; // index for A

        // Merge L and R into A[p..r]
        while (i < nL && j < nR) {
            if (L[i] <= R[j]) {
                A[k] = L[i];
                i++;
            } else {
                A[k] = R[j];
                j++;
            }
            k++;
        }

        // Copy any remaining elements of L
        while (i < nL) {
            A[k] = L[i];
            i++;
            k++;
        }

        // Copy any remaining elements of R
        while (j < nR) {
            A[k] = R[j];
            j++;
            k++;
        }
    }
}


