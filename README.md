// Train Problem


class Main {
    public static void main(String[] args) {
        int arr[] = { 900, 940, 950, 1100, 1500, 1800};
        int dep[] = { 910, 1200, 1120, 1130, 1900, 2000};
        int platform =0, max=1,i=0,j=0;
        while(j < dep.length ){
            if(arr[i]<dep[j] && i < arr.length -1){
                platform ++;
                i++;
            }
            else{
                j++;
                if(platform>max)
                    max=platform;
                platform--;
            }
        }
        System.out.println("Number of platform required is: "+max);
    }
}

// Output: Number of platform required is: 3
