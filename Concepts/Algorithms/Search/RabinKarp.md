# Rabin Karp Algorithm

Simple Text Search algorithm is very inefficient when patterns are long and when there is a lot of repeated elements of the pattern.

The idea of Rabin Karp algorithm is to use hashing to find a pattern in a text. At the beginning of the algorithm, we need to calculate a hash of the pattern which is later used in the algorithm. This process is called fingerprint calculation, and we can find a detailed explanation here.

The important thing about pre-processing step is that its time complexity is O(m) and iteration through text will take O(n) which gives time complexity of whole algorithm O(m+n).

In worst-case scenario, time complexity for this algorithm is O(m(n-m+1)). However, on average this algorithm has O(n+m) time complexity.

```
public static int RabinKarpMethod(char[] pattern, char[] text) {
    int patternSize = pattern.length;
    int textSize = text.length;      

    long prime = getBiggerPrime(patternSize);

    long r = 1;
    for (int i = 0; i < patternSize - 1; i++) {
        r *= 2;
        r = r % prime;
    }

    long[] t = new long[textSize];
    t[0] = 0;

    long pfinger = 0;

    for (int j = 0; j < patternSize; j++) {
        t[0] = (2 * t[0] + text[j]) % prime;
        pfinger = (2 * pfinger + pattern[j]) % prime;
    }

    int i = 0;
    boolean passed = false;

    int diff = textSize - patternSize;
    for (i = 0; i <= diff; i++) {
        if (t[i] == pfinger) {
            passed = true;
            for (int k = 0; k < patternSize; k++) {
                if (text[i + k] != pattern[k]) {
                    passed = false;
                    break;
                }
            }

            if (passed) {
                return i;
            }
        }

        if (i < diff) {
            long value = 2 * (t[i] - r * text[i]) + text[i + patternSize];
            t[i + 1] = ((value % prime) + prime) % prime;
        }
    }
    return -1;

}
```
