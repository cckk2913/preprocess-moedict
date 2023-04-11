# preprocess-moedict
preprocessing word sense information in moedict-data

After cloning the repos (https://github.com/g0v/moedict-data.git, https://github.com/g0v/moedict-epub.git), 
    
    you get `moedict-data/dict-revised.json`.

`dict-revised.json` is a list of dictionaries.

Each dictionary:
```
(1st level) keys: 'heteronyms', 'title'
(2nd level)  heteronyms : [{definitions:[], bopomofo, pinyin}] # 後兩者可能為空
(3rd level)  definitions(list of senses) : 
                    [
                      {def, 
                        quote:[], example:[],   #不一定有
                        synonyms:'A,B', anotonyms:'A,B',   #不一定有
                        type:'動',   #不一定有
                      },
                      {第二個sense def 同上},
                      {第三個sense def 同上}...       
                    ]
```
