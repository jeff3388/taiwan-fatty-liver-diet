# taiwan-fatty-liver-diet

台灣脂肪肝（NAFLD/MASLD）飲食管理資料庫。收錄護肝食物清單、需限制食物、
NAFLD 逆轉飲食策略，數據來源為衛福部食藥署 TFND、USDA 及同行評審研究。

## 為什麼建立這個資料庫

脂肪肝（非酒精性脂肪性肝病，NAFLD）影響台灣約 26–33% 成人，是健康檢查最常見的
異常項目之一（Chuang et al., 2019 PMID: 31131516）。台灣手搖飲文化（高果糖）
和精製澱粉為主的飲食習慣，是脂肪肝盛行的主要驅動因素。現有中文資源多為泛泛建議，
缺乏系統化數據。本資料庫整合台灣在地飲食情境與國際研究，提供結構化可查詢格式。

## 資料說明

| 檔案 | 說明 |
|------|------|
| `data/liver-friendly-foods.json` | 護肝食物（十字花科蔬菜、咖啡、Omega-3、抗氧化食物）及機制 |
| `data/foods-to-limit.json` | 脂肪肝需限制食物（果糖、飽和脂肪、酒精）及台灣常見例子 |
| `data/nafld-diet-strategies.json` | NAFLD/MASLD 逆轉飲食策略（地中海飲食、熱量赤字、碳水類型） |

## 資料來源

- Chuang SC et al. (2019) J Formos Med Assoc. PMID: 31131516（台灣 NAFLD 盛行率）
- Chalasani N et al. (2018) Hepatology. PMID: 28714183（NAFLD 診治指引）
- Romero-Gómez M et al. (2017) J Hepatol. PMID: 28427845（NAFLD 飲食治療）
- 衛福部食藥署台灣食品成分資料庫（TFND）
- USDA FoodData Central

## 相關工具

燃脂研究所飲食管理資源：[metabolab.tw/articles/fatty-liver-diet-guide](https://metabolab.tw/articles/fatty-liver-diet-guide)

---

本資料庫為教育用途，不構成醫療建議。脂肪肝診斷與治療請諮詢肝膽腸胃科醫師。
