```java

 public static int romanToInt(String s) {
        Integer result = 0;
        Integer previous = 0;
        Integer next = 0;
        Integer current = 0;

        Map<String, Integer> standardMap = new HashMap<>();
        standardMap.put("I", 1);
        standardMap.put("V", 5);
        standardMap.put("X", 10);
        standardMap.put("L", 50);
        standardMap.put("C", 100);
        standardMap.put("D", 500);
        standardMap.put("M", 1000);




        List<String> numeralList = new ArrayList<>(Arrays.asList(s.split("")));
        for(int i = 0; i < numeralList.size(); i++){
            current = standardMap.get(numeralList.get(i));

            if(i+1 >= numeralList.size()){ //index does not exists
                result += standardMap.get(numeralList.get(i));
            }else { // index exists
                next = standardMap.get(numeralList.get(i + 1));
                if (previous == 0){
                    previous = standardMap.get(numeralList.get(i));
                    if (current >= next) {
                        result += standardMap.get(numeralList.get(i));
                    } else {
                        result -= standardMap.get(numeralList.get(i));
                    }
                    continue;
                }
                if (current >= next) {
                    result += standardMap.get(numeralList.get(i));
                } else {
                    result -= standardMap.get(numeralList.get(i));
                }
            }
        }

        return result;
    }


    //convert string to roman numerals
    public static int romanToInts(String s) {
        int res = 0;
        int nums = 0;
        int prev = 0;
        for(int i = s.length() - 1; i >= 0; i--){
            //getting value of symbol s[i]
            switch(s.charAt(i)){
                case 'I' : nums = 1; break;
                case 'V' : nums = 5; break;
                case 'X' : nums = 10; break;
                case 'L' : nums = 50; break;
                case 'C' : nums = 100; break;
                case 'D' : nums = 500; break;
                case 'M' : nums = 1000; break;
            }
            if( prev > nums){
                res = res - nums;
            }else{
                res = res + nums;
            }
            prev = nums;
        }
        return res;
    }
```