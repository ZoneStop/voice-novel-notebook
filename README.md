# 🎙️ Voice Novel Notebook

[English](#english) | [ภาษาไทย](#ภาษาไทย)

> 🚧 **Status: planning / early development**

---

## English

A browser-based notebook for writing novels and documents **by speaking** — built to be stable enough for real, long-form writing.

### Why this project exists
I want to write novels and work documents, but typing is slow — sometimes the idea slips away before I finish typing it.
Apps with speech-to-text features often produce distorted text, and when I mix languages the output gets jumbled. Fixing it takes so long that it's not usable for real work.
So I want a tool that transcribes more reliably and is actually practical for writing.

### Common problems with existing speech-to-text apps
- Switching between Thai and English mid-speech produces garbled text
- Frequent mis-transcriptions — fixing them takes as long as typing
- Accents make results unstable (e.g. pronouncing ร /r/ as ล /l/)
- Transliterated words (loanwords) come out inconsistently

### Planned approach
- **Language switch by keyboard shortcut** — switch the recognition model between Thai and English, so each part is handled by a model made for that language. This also lets the writer decide how loanwords are written (e.g. "คอมพิวเตอร์" vs "computer").
- **Pause listening by keyboard shortcut** — stop recognition temporarily during breaks so unwanted sounds don't end up in the text.
- **AI clean-up step** — speech recognition hears sounds, not meaning. An AI language model can read the whole sentence and fix mis-heard words from context (e.g. "ลิมแม่น้ำ" → "ริมแม่น้ำ"), add punctuation, and keep a custom list of character names and terms.

### Progress
- [ ] Level 1: Press a button → speak → Thai text appears on screen
- [ ] Level 2: Continuous dictation, text keeps appending
- [ ] Level 3: Edit text manually + keep notes after closing the page
- [ ] Level 4: Keyboard shortcuts — switch language (TH ↔ EN) and pause listening
- [ ] Level 5: AI clean-up button + custom word list (character names, places)
- [ ] Level 6: Try alternative recognition engines (e.g. Thai-specific models) for better accuracy

### Roadmap (later)
- Customisable keyboard shortcuts — pick the keys you're comfortable with
- More languages: Chinese, Japanese, Korean
- Export to common formats

### Limitations
- Speech recognition is an external service (the browser's Web Speech API), not built into this app
- Requires an internet connection; audio is sent to the provider's servers for processing
- Initial support: **2 languages — Thai and English**

### Tech
HTML · JavaScript · Web Speech API (Chrome)

### How to use
*Coming soon — after Level 1 is done.*

---

## ภาษาไทย

สมุดบันทึกบนเบราว์เซอร์ สำหรับเขียนนิยายและงานเอกสาร**ด้วยการพูด** ตั้งใจให้เสถียรพอจะใช้เขียนงานยาวได้จริง

### ทำไมถึงมีโปรเจกต์นี้
อยากเขียนนิยายหรือพิมพ์งาน แต่ขี้เกียจพิมพ์ บางครั้งพิมพ์ไปแล้วไอเดียหลุดหายไปก่อน
พอลองใช้แอปที่มีฟีเจอร์พูดเป็นข้อความ มักเจอปัญหาข้อมูลเพี้ยน พูดแล้วภาษาปนกัน ทำให้เสียเวลาต้องแก้ไข จนรู้สึกว่าถ้าเป็นแบบนี้จะใช้ทำงานจริงไม่ได้
เลยอยากมีโปรแกรมที่ถอดเสียงได้เสถียรกว่า และใช้งานได้จริง

### ปัญหาที่เจอในแอปถอดเสียงทั่วไป
- พูดสลับไทย-อังกฤษแล้วข้อความเพี้ยน
- ถอดเสียงผิดบ่อย ต้องเสียเวลาแก้จนไม่ต่างจากพิมพ์เอง
- สำเนียงต่างกัน ทำให้คำที่ได้ไม่เสถียร เช่น ออกเสียง ร เป็น ล
- คำทับศัพท์ออกมาไม่สม่ำเสมอ

### แนวทางแก้ (แผน)
- **สลับภาษาด้วยคีย์ลัด** สลับโมเดลฟังเสียงระหว่างไทยกับอังกฤษ ให้แต่ละช่วงใช้โมเดลที่เก่งภาษานั้นจริง และให้คนเขียนเลือกได้เองว่าคำทับศัพท์จะออกมาแบบไหน (เช่น "คอมพิวเตอร์" หรือ "computer")
- **พักการฟังด้วยคีย์ลัด** หยุดฟังชั่วคราวตอนพัก ป้องกันเสียงที่ไม่ต้องการเข้าไปในข้อความ
- **ขั้นเกลาด้วย AI** ระบบถอดเสียงฟังแค่เสียง ไม่รู้ความหมาย แต่ AI ภาษาอ่านบริบททั้งประโยคได้ จึงแก้คำที่ถอดผิดได้ (เช่น "ลิมแม่น้ำ" → "ริมแม่น้ำ") ใส่วรรคตอน และใช้ลิสต์ชื่อตัวละครหรือคำเฉพาะที่กำหนดเอง

### ความคืบหน้า
- [ ] ด่าน 1: กดปุ่ม → พูด → ข้อความไทยขึ้นจอ
- [ ] ด่าน 2: พูดต่อเนื่องได้ยาว ข้อความต่อท้ายไปเรื่อยๆ
- [ ] ด่าน 3: แก้ข้อความเองได้ + บันทึกไม่หายตอนปิดหน้า
- [ ] ด่าน 4: คีย์ลัดสลับภาษา (ไทย ↔ อังกฤษ) และพักการฟัง
- [ ] ด่าน 5: ปุ่มเกลาด้วย AI + ลิสต์คำเฉพาะ (ชื่อตัวละคร สถานที่)
- [ ] ด่าน 6: ลองเครื่องยนต์ถอดเสียงอื่น (เช่น โมเดลเฉพาะภาษาไทย) เพื่อความแม่นยำ

### แผนพัฒนาต่อ
- ตั้งคีย์ลัดเองได้ เลือกปุ่มที่ถนัด
- เพิ่มภาษา: จีน ญี่ปุ่น เกาหลี
- ส่งออกเป็นไฟล์รูปแบบทั่วไป

### ข้อจำกัด
- เครื่องฟังเสียงเป็นบริการภายนอก (Web Speech API ของเบราว์เซอร์) ไม่ใช่ของตัวแอปเอง
- ต้องต่ออินเทอร์เน็ต และเสียงจะถูกส่งไปประมวลผลที่เซิร์ฟเวอร์ของผู้ให้บริการ
- ช่วงเริ่มต้นรองรับ **2 ภาษา: ไทย และอังกฤษ**

### เทคโนโลยีที่ใช้
HTML · JavaScript · Web Speech API (Chrome)

### วิธีใช้
*จะเพิ่มหลังผ่านด่าน 1*
