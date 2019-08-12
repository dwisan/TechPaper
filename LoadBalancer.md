>Load Balancer คืออะไร?

Load Balancer คือระบบที่ทำหน้าที่ในการกระจาย Request จาก User แต่ละคนไปยัง Server จำนวนหลายๆ เครื่อง เพื่อให้ Server แต่ละเครื่องให้บริการ User แต่ละคนได้ตามประสิทธิภาพที่ตนเองมี หรือเพื่อลด Downtime ของระบบโดยให้ Server เครื่องที่ยังสามารถให้บริการ User ได้คอยรับ Request จาก User แทนเครื่อง Server ที่หยุดทำงานไปแล้ว ดังนั้นโดยสรุปแล้ว Load Balancer จะมีบทบาทดังนี้
เพิ่มประสิทธิภาพให้ระบบ Application แบบ Scale-out ด้วยการทำ Load Balancing

ด้วยการทำ Server Load Balancing ร่วมกันระหว่าง Server หลายๆ เครื่อง และตั้ง Policy ในการกระจายโหลดตามประสิทธิภาพของแต่ละเครื่อง หรือตาม IP/Session เพื่อให้ Server หลายๆ เครื่องช่วยกันให้บริการ User หลายๆ คนพร้อมๆ กัน โดย User แต่ละคนยังถูก Redirect ไปยังเครื่อง Server เครื่องที่ตนเองมี Session อยู่เสมอ
ทำให้ระบบ Application ทำงานได้แบบ High Availability

โดยการทำ Server Load Balancing ร่วมกันระหว่าง Server หลายๆ เครื่อง และเมื่อเครื่องใดเครื่องหนึ่งหยุดทำงานไป Load Balancer จะสามารถตรวจพบและทำการ Redirect User ไปใช้งาน Server เครื่องที่ยังคงทำงานอยู่
ทำให้ระบบ Application มีความทนทานระดับ Disaster Recovery

ด้วยการทำ Global Server Load Balancing ร่วมกันระหว่าง Data Center ที่อยู่ต่างสาขากันด้วยเทคนิคการประยุกต์ใช้ DNS ทำให้เมื่อ Application ใดๆ ใน Data Center ใดๆ หยุดทำงานไป ผู้ใช้งานจะถูก Redirect ไปยัง Application เดียวกันที่อยู่ต่าง Data Center โดยอัตโนมัติ รองรับทั้งการกระจาย Application ไว้ตาม Data Center ต่างๆ ทั่วโลกเพื่อลด Network Latency ลง และการทำ Real-time Disaster Recovery ไปพร้อมๆ กัน
