private static class MaximalInd {

    private int maxValue;
    private int maxIndex;
    public MaxElement(final int maxValue, final int maxIndex) {
        this.maxIndex = maxIndex;
        this.maxValue = maxValue;
    }

    @Override
    public String toString() {
        return String.format("MaxValue = {%d}, MaxIndex = {%d}", maxValue, maxIndex);
    }
}

public static void main(String[] args) {

    int[] a = new int[10];
    Random rand = new Random();
    for (int i = 0; i < a.length; i++) {
        int n = rand.nextInt(100);
        a[i] = n;
    }

    System.out.println(Arrays.toString(a));
    System.out.println(" maximalnii  index : " + findIndexOfMaxValueLinearSearch(a));


}

private static MaxElement findIndexOfMaxValueLinearSearch(int[] a) {
    int maxValue = 0;
    int maxIndex = -1;
    for (int i = 0; i < a.length; i++) {
        if (a[i] > maxValue) {
            maxValue = a[i];
            maxIndex = i;
        }
    }

    return new MaxElement(maxValue, maxIndex);
}
}
