# ฟังเสียงโซเชียล · Doctor's Feud

เกม Family Feud ธีม Social Listening สำหรับงานของแพทย์อาวุโสและผู้บริหารโรงพยาบาล

## วิธีใช้
เปิด `index.html` บนเบราว์เซอร์ หรือฉายขึ้นจอ — คลิกช่องเพื่อเปิดคำตอบ

- ← → : เลื่อนข้อ
- 1–6 : เปิดช่องคำตอบ
- x : strike

เป็นไฟล์ static ไม่มี backend เล่นได้บนทุกเบราว์เซอร์และมือถือ

## แก้คำถาม / คำตอบ / คะแนน
เปิดไฟล์ `questions.js` แก้ array `QUESTIONS` ได้เลย แต่ละข้อมีรูปแบบ:

```js
{ q: "คำถาม", a: [ ["คำตอบ", คะแนน], ["คำตอบ", คะแนน], ... ] }
```

- เรียงคำตอบจากคะแนนมากไปน้อย (ลำดับนี้คือลำดับช่องบนกระดาน 1-6)
- เพิ่ม/ลบคำถามได้ตามต้องการ ไม่ต้องแก้ไฟล์อื่น

## แก้ข้อความแบรนด์ (eyebrow + ชื่อเกม)
แก้ออบเจ็กต์ `BRAND` ในไฟล์ `questions.js` เดียวกัน:

```js
const BRAND = {
  eyebrow: "Social Listening Edition",
  titlePrefix: "ฟังเสียงโซเชียล",
  titleAccent: "·",
  titleSuffix: "Doctor's Feud",
};
```

`titleAccent` คือส่วนที่ขึ้นสีทองตรงกลางชื่อเกม

## Deploy (GitHub Pages)
Settings → Pages → Source: Deploy from a branch → `main` / `(root)` → Save
URL: `https://<username>.github.io/<repo>/`
