# การตั้งค่า LLM ในเครื่องด้วย LM Studio และ OpenWebUI

คู่มือนี้สรุปขั้นตอนการตั้งค่า Large Language Model (LLM) ในเครื่องโดยใช้ LM Studio และเชื่อมต่อกับ OpenWebUI เพื่ออินเทอร์เฟซการแชทที่ใช้งานง่าย

## คำแนะนำในการตั้งค่า

### 1. ตั้งค่า LM Studio

1.  **ดาวน์โหลดและติดตั้ง:** รับ LM Studio จาก [https://lmstudio.ai/](https://lmstudio.ai/) และติดตั้งบนระบบของคุณ
2.  **ดาวน์โหลดโมเดล:** เปิด LM Studio ใช้ส่วน "Discover" หรือ "Chat" เพื่อค้นหาและดาวน์โหลดโมเดลภาษาที่คุณต้องการใช้
3.  **เริ่มเซิร์ฟเวอร์ในเครื่อง:**
    *   ไปที่แท็บ "Local Server" ใน LM Studio
    *   เลือกโมเดลที่คุณดาวน์โหลดจากเมนูแบบเลื่อนลง
    *   คลิก "Start Server" ซึ่งจะเรียกใช้เซิร์ฟเวอร์อนุมานในเครื่องของคุณ โดยทั่วไปจะอยู่ที่พอร์ต 1234

### 2. เชื่อมต่อ OpenWebUI กับ LM Studio

1.  **เปิด OpenWebUI:** เปิด OpenWebUI ในเว็บเบราว์เซอร์ของคุณ
2.  **ไปที่การเชื่อมต่อ:** คลิกที่ไอคอนโปรไฟล์ของคุณที่มุมบนขวา จากนั้นไปที่ "Admin Panel" -> "Settings" -> "Connections" -> "OpenAI API"
3.  **แก้ไขการเชื่อมต่อ:**
    *   คลิก "Edit Connections"
    *   **URL:**
        *   หากคุณใช้ OpenWebUI ใน Docker ให้ใช้ `http://host.docker.internal:1234/v1`
        *   หากคุณใช้ OpenWebUI โดยตรงบนเครื่องโฮสต์ของคุณ ให้ใช้ `http://localhost:1234/v1`
    *   **Auth:** เลือก "None"
4.  **บันทึกและแชท:**
    *   คลิก "Save"
    *   ตอนนี้คุณควรจะสามารถแชทกับ LLM ในเครื่องของคุณผ่าน OpenWebUI ได้แล้ว

## อ้างอิง

*   [เอกสาร OpenWebUI: การเริ่มต้นใช้งานร่วมกับ OpenAI](https://docs.openwebui.com/getting-started/quick-start/starting-with-openai-compatible)