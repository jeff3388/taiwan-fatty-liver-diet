# Taiwan Fatty Liver Diet Database（台灣脂肪肝飲食管理資料庫）

台灣 NAFLD/MASLD 飲食管理結構化資料庫。收錄護肝食物清單、需限制食物、NAFLD 逆轉飲食策略與台灣在地飲食情境分析，數據來源為衛福部食藥署 TFND、USDA 及同行評審研究。

## 為什麼建立這個資料庫

脂肪肝（非酒精性脂肪性肝病，NAFLD，現更名為 MASLD—代謝相關脂肪性肝病）影響台灣約 **26–33% 成人**，是健康檢查最常見的異常項目之一（Chuang et al., 2019）。

**台灣特有的高風險因素：**

| 風險因素 | 台灣情境 |
|---------|---------|
| 高果糖飲料 | 手搖飲市場規模超過 750 億元，人均年消費量全球前三 |
| 精製澱粉主食 | 白米飯、麵食為主，升糖負荷高 |
| 外食比例 | 台灣外食率超過 70%，油脂和熱量控制困難 |
| 代謝症候群 | 台灣代謝症候群盛行率約 26%，與 NAFLD 高度重疊 |
| 洗腎率 | 台灣洗腎率全球最高，NAFLD 是 CKD 的獨立危險因子 |

多數台灣 NAFLD 患者在早中期**完全無症狀**——這也是為什麼「肝有點油，沒關係」的心態如此危險。

## NAFLD 的代謝機制

```
果糖過量攝取
    ↓
肝臟 De Novo 脂質合成（DNL）增加
    ↓
VLDL 合成受阻（膽鹼不足時加重）
    ↓
肝內脂肪積累（脂肪肝 Grade 1–3）
    ↓
NASH（肝臟發炎）→ 纖維化 → 肝硬化
```

**胰島素抗性的惡性循環：**
脂肪肝加重胰島素抗性 → 更多游離脂肪酸流入肝臟 → 更多脂肪積累 → 循環持續。

## 資料說明

| 檔案 | 說明 |
|------|------|
| `data/liver-friendly-foods.json` | 護肝食物（十字花科蔬菜、咖啡、Omega-3、抗氧化食物）及機制 |
| `data/foods-to-limit.json` | 脂肪肝需限制食物（果糖、飽和脂肪、酒精）及台灣常見例子 |
| `data/nafld-diet-strategies.json` | NAFLD/MASLD 逆轉飲食策略（地中海飲食、熱量赤字、碳水類型） |

## 逆轉脂肪肝的飲食策略（有 RCT 證據）

| 策略 | 效果 | 證據等級 |
|------|------|---------|
| 減重 7% 體重 | 組織學改善 NAFLD | A（多個 RCT） |
| 減重 10% 體重 | 可逆轉 NASH（含纖維化） | A |
| 去除液態果糖（手搖飲、果汁） | 8–12 週內顯著降低肝臟脂肪 | A |
| 地中海飲食模式 | 比低脂飲食更有效改善 NAFLD | A（2023 meta-analysis） |
| 每日 2–3 杯黑咖啡 | 肝臟纖維化風險降低 40% | B（觀察性，一致） |
| 每週 150 分鐘有氧運動 | 直接減少肝臟脂肪（不需體重下降） | A |

## 台灣高風險食物：需限制

**最需要減少的前 5 項（台灣情境）：**

1. **手搖飲（全糖）**：一杯大杯全糖珍奶含果糖約 40–60g，直接觸發 DNL
2. **火鍋湯底（久煮）**：高油脂 + 高普林，同時傷肝傷腎
3. **精製澱粉 + 含糖醬料**：白飯搭配甜辣醬、沙茶醬，升糖+高果糖組合
4. **夜市炸物**：高飽和脂肪 + 反覆加熱油脂
5. **酒精（任何形式）**：即使是「適量」，台灣約 50% 人帶有 ALDH2 基因，乙醛清除慢，對肝傷害更大

## 護肝食物：優先攝取

| 食物類別 | 代表食材 | 機制 |
|---------|---------|------|
| 十字花科蔬菜 | 花椰菜、高麗菜、青花椰 | Sulforaphane 誘導 Phase 2 解毒酶 |
| Omega-3 食物 | 鯖魚、秋刀魚、亞麻籽 | 降低 TG、抗肝臟發炎 |
| 黑咖啡 | 現泡黑咖啡（無糖） | 多酚保護肝細胞，降低纖維化風險 |
| 高纖維食物 | 燕麥、豆類、地瓜（含皮） | 改善腸道菌相，減少腸漏症風險 |
| 低脂乳製品 | 無糖優格、低脂牛奶 | 乳清蛋白促進尿酸排泄，降低果糖衝擊 |
| 綠茶（無糖） | 台灣高山烏龍（現泡） | EGCG 抗氧化，改善脂質代謝 |

## 資料格式範例

```json
{
  "food_id": "fl_001",
  "name_zh": "花椰菜",
  "name_en": "Broccoli",
  "category": "liver_friendly",
  "mechanism": "sulforaphane_phase2_induction",
  "evidence_level": "B",
  "serving_g": 100,
  "calories_kcal": 34,
  "notes": "輕蒸 3–5 分鐘保留最多 Sulforaphane；微波也可"
}
```

## 資料來源

- Chuang SC et al. (2019) J Formos Med Assoc. **PMID: 31131516**（台灣 NAFLD 盛行率 26–33%）
- Chalasani N et al. (2018) Hepatology. **PMID: 28714183**（AASLD NAFLD 診治指引）
- Romero-Gómez M et al. (2017) J Hepatol. **PMID: 28427845**（NAFLD 飲食治療系統性回顧）
- Zelber-Sagi S et al. (2023) J Hepatol. **PMID: 36813120**（地中海飲食 vs 低脂飲食 RCT）
- Wijarnpreecha K et al. (2017) Eur J Gastroenterol Hepatol. **PMID: 28009748**（咖啡與 NAFLD Meta-analysis）
- 衛福部食藥署台灣食品成分資料庫（TFND）
- USDA FoodData Central

## 相關工具（Interactive Tools）

本資料庫的 NAFLD 飲食科學，已整合至 [MetaboLab](https://metabolab.tw) 的互動工具中：

- 📊 **[TDEE 計算機](https://metabolab.tw/calculators/tdee)**：設計 500–750 kcal 的每日熱量赤字——減重 7–10% 是逆轉 NAFLD 最有力的單一介入，TDEE 計算是起點。
- 🥗 **[211 餐盤計算機](https://metabolab.tw/calculators/211-meal-plan)**：建立以蔬菜（十字花科優先）、蛋白質（魚類 Omega-3）、全穀為主的地中海式飲食框架——這是目前 RCT 支持對 NAFLD 最有效的飲食模式。
- 📏 **[腰圍風險計算機](https://metabolab.tw/calculators/waist-risk)**：腰圍是 NAFLD 最準確的臨床預測指標之一（比 BMI 更準），追蹤腰圍縮小是評估脂肪肝改善最實用的方法。
- 🔢 **[熱量換算工具](https://metabolab.tw/calculators/calorie-converter)**：量化台灣手搖飲和外食的熱量，建立「液態果糖 = 直接喂養脂肪肝」的真實感知。

---

本資料庫為教育用途，不構成醫療建議。脂肪肝診斷（超音波分級）與進階治療請諮詢肝膽腸胃科醫師。

## License

MIT © taiwan-fatty-liver-diet contributors
