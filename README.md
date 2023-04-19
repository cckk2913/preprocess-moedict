# Preprocess-moedict
The main goal is to extract and pre-process word sense information from the moedict-data (by 教育部國語推行委員會). After running the first 5 cell blocks in the notebook,  you get `moedict-data/dict-revised.json`.

- `dict-revised.json` is a list of dictionaries.

- The composition of one dictionary:
  ```
  (1st level) keys: "heteronyms", "title", "non_radical_stroke_count", "radical", "stroke_count"
  (2nd level)  heteronyms : 
                    [
                      {definitions: list of dictionaries, ## each dictionary represents a sense
                      bopomofo: str, 
                      pinyin: str}
                    ] 
  (3rd level)  definitions(list of senses) : 
                    [
                      {def: str, 
                        quote: list (of strings), 
                        example: list (of strings),   
                        synonyms: str,              ## each synonym is separated by ',' 
                        anotonyms: str,             ## each antonym is separated by ',' 
                        type: str,   
                      },
                      {第二個sense def 同上},
                      {第三個sense def 同上}...       
                    ]
  ```

----------------------------------------------------


這是將「重編國語辭典（修訂本）」的公眾授權內容處理為機器比較容易再利用的 json 格式。辭典本文的著作權仍為教育部所有。

公眾授權網：https://language.moe.gov.tw/001/Upload/Files/site_content/M0001/respub/index.html

依教育部之解釋，「創用CC-姓名標示- 禁止改作 臺灣3.0版授權條款」之改作限制標的為文字資料本身，不限制格式轉換及後續應用。

```
=====================================================

企劃執行：國家教育研究院

原 著 者：教育部國語推行委員會
　　　   （民國102年1月1日配合行政院組改併入相關單位）

發 行 人：潘文忠　林崇熙

發 行 所：中華民國教育部

維護單位：國家教育研究院語文教育及編譯研究中心

地　　址：臺北市大安區和平東路一段179號

電　　話：(02)7740-7282

傳　　真：(02)7740-7284

電子郵件：onile@mail.naer.edu.tw

版　　次：中華民國110年11月臺灣學術網路第六版

=====================================================
```

此處轉換格式、重新編排的編輯著作權（如果有的話）由 @kcwu 以 CC0 釋出。

