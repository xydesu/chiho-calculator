# 移動距離計算機

> maimai DX「地方巡業」移動距離計算工具

🔗 **線上版本：** <https://xydesu.github.io/chiho-calculator/>

---

## 預覽

![畫面預覽](https://raw.githubusercontent.com/xydesu/chiho-calculator/refs/heads/main/docs/MainUI.png)

---

## 功能特色

- **一鍵計算** 本次出行可獲得的移動距離
- **反推計算** 距離目標還需幾道（幾局）以及總花費
- **加速券支援** 可選擇 2 倍 / 3 倍加速券，自動計入費用
- **成員設定** 分別標記每位成員是否「擅長」，精確計算 Deluxe Power
- **深色模式** 自動偵測系統偏好，並可手動切換
- **表單記憶** 設定值透過 localStorage 自動儲存，重開頁面不流失

---

## 輸入說明

| 欄位 | 說明 |
|------|------|
| 成員 | 隊長固定為「擅長」(+4 Km)；其餘 4 位成員可分別勾選是否擅長（擅長 +2 Km，不擅長 +1 Km） |
| 獎勵樂曲 | 若本次包含獎勵樂曲，額外 +2 Km |
| 遊玩獎勵 | 2 人以上或邀請 +1 / FULL COMBO +2 / ALL PERFECT +3 / FULL SYNC +4 Km |
| 遊玩曲數 | 本次遊玩的曲目數（3 或 4 曲） |
| 加速券 | 無 / 2 倍加速券（+1 道費用）/ 3 倍加速券（+2 道費用） |
| 每道價格 | 每局的遊玩費用（單位：元） |
| 目標距離 | 希望達成的總移動距離（單位：Km） |

---

## 計算公式

```
Deluxe Power = 隊長 × 4 + 擅長成員數 × 2 + 不擅長成員數 × 1

本次移動距離 = ⌈ (Deluxe Power + 遊玩獎勵 + 樂曲獎勵) × 曲目數 × 票券倍率 ⌉

所需道數 = ⌈ 目標距離 ÷ 本次移動距離 ⌉
總花費   = 每道費用 × 所需道數
```

---

## 相關連結

- [maimai 攻略 Wiki (gamerch)](https://gamerch.com/maimai/)
- [GitHub 專案頁面](https://github.com/xydesu/chiho-calculator/)
