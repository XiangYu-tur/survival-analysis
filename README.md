# 一、資料集介紹
    
本次使用資料為德國乳腺癌研究組(GBSG)於1984年7月到1989年12月召募了720名原發性淋巴結陽性乳腺癌患者，以研究3和6週期的化療和使用tamoxifen(泰莫西芬)進行額外激素治療的有效性。
     
- Tamoxifen   
    
  抗雌激素Tamoxifen (泰莫西芬)是早期的標準荷爾蒙治療選擇，可使用於不管停經前停經後，淋巴結轉移與否，只要荷爾蒙受體陽性(ER+)皆可適用。
   
### 變數介紹: 

|變數|定義|
|:---|:---|
|pid|患者ID|
|age|年齡(年)|
|meno|更年期狀態(0 = 停經前, 1 = 停經後)|　　
|size|腫瘤大小(mm)|　　　　
|grade|腫瘤分級|　　　
|nodes|陽性淋巴結數|　
|pgr|孕激素受體(fmol/l) 是一種會在乳房、卵巢、子宫和子宫頸中作用的蛋白質受體。|
|er|雌激素受體(fmol/l)|　
|hormon|是否接受激素療法(0= 否, 1 = 是)|　　　
|rfstime|復發、死亡或失去追蹤時間|　　　
|status|0 = 存活, 1 = 死亡|　　　　　

   
# 二、研究目的
   
本次分析希望藉由此資料集來分析上述變數中對於乳癌影響程度的嚴重性與重要性，並依照下列步驟找出對於乳癌患者來說影響其生存時間的重要因素。
   
(1) 藉由Kaplan-Meierc繪出在相同更年期狀態下是否接受激素療法與否，與同樣接受或沒接受雌激素療法下不同更年期狀態之存活曲線。
     
(2) 藉由Log-rank test檢驗上述兩組之間存活時間是否有顯著差異。
    
(3) 藉由cox model計算在不同狀態下風險比例的差異。
    
(4) 將我們有興趣的變數加入迴歸模型中，並因應資料使用相對應的分佈來分析不同狀況的病人風險比例的差異。
