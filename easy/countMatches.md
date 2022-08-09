```java
//    Question:
//    You are given an array items, where each items[i] = [typei, colori, namei] describes the type, color, and name of the ith item. You are also given a rule represented by two strings, ruleKey and ruleValue.
//
//            The ith item is said to match the rule if one of the following is true:
//
//            ruleKey == "type" and ruleValue == typei.
//            ruleKey == "color" and ruleValue == colori.
//            ruleKey == "name" and ruleValue == namei.

//            Return the number of items that match the given rule.

```
```java
//    Most optimal solution:
        public int countMatches(List<List<String>> items, String ruleKey, String ruleValue) {
            int res = 0;
    
            for(int i = 0 ;i<items.size();i++){
                if(ruleKey.equals("type") && items.get(i).get(0).equals(ruleValue)) res++;
                if(ruleKey.equals("color") && items.get(i).get(1).equals(ruleValue)) res++;
                if(ruleKey.equals("name") && items.get(i).get(2).equals(ruleValue)) res++;
            }
    
            return res;
    
        }

``` 
```java
    
//   My first solution
    public int countMatches(List<List<String>> items, String ruleKey, String ruleValue) {
        int numberOfMatches = 0;
        List<String> typeList = new ArrayList<>();
        List<String> colorList = new ArrayList<>();
        List<String> nameList = new ArrayList<>();
        items.forEach((item) -> {
            typeList.add(item.get(0));
            colorList.add(item.get(1));
            nameList.add(item.get(2));
        });
        if (ruleKey.equals("type")){
          numberOfMatches =  Collections.frequency(typeList, ruleValue);
        }
        if (ruleKey.equals("color")){
          numberOfMatches =  Collections.frequency(colorList, ruleValue);
        }
        if (ruleKey.equals("name")){
          numberOfMatches =  Collections.frequency(nameList, ruleValue);
        }
        
        return numberOfMatches;
    }
    
```