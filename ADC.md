Application Delivery Controller หรือ ADC ได้ถูกพัฒนาต่อยอดมาจาก Load Balancer โดยการเพิ่มความสามารถต่างๆ ที่จะช่วยเพิ่มประสิทธิภาพ, ลด Bandwidth และเพิ่มความปลอดภัยให้แก่ Application ไปพร้อมๆ กัน โดยสรุปแล้ว Application Delivery Controller จะมีบทบาทดังนี้

- [x] ทำทุกความสามารถของ Load Balancer ได้

การออกแบบระบบ Application ให้รองรับการ Scale-out, High Availability และ Disaster Recovery สามารถทำได้ทั้งหมดภายใน Application Delivery Controller เพียงชุดเดียว และรองรับตั้งแต่การทำ Load Balancer ด้วยการตรวจจับเงื่อนไขจากข้อมูลเครือข่ายที่ระดับ Layer 2 ถึง Layer 7 เพื่อให้การกำหนดนโยบายในการทำ Load Balancing เหมาะสมกับ Application ได้อย่างสูงสุด

- [x] SSL Encryption Offload

เป็น Option เสริมเพื่อติดตั้ง Hardware SSL Acceleration เพื่อทำการเข้ารหัสด้วย SSL แทน Application Server ทำให้ Application Server ต่างๆ สามารถลดการทำงานของ CPU ลงได้อย่างมหาศาล และยังเข้ารหัสด้วย Application Delivery Controller ได้รวดเร็วยิ่งขึ้นอีกด้วย ทำให้เครื่อง Server ที่มีสเป็คและจำนวนเท่าเดิม สามารถรองรับผู้ใช้่งานได้จำนวนมากขึ้น และให้บริการรวดเร็วขึ้นด้วย

- [x] TCP Connection Multiplexing

Application Delivery Controller จะช่วยลดจำนวนการเชื่อมต่อของ TCP ที่ Application Server ได้ โดยการรับบทบาทเป็นผู้เชื่อมต่อ TCP กับ User ทั้งหมดเอง และสร้าง TCP Conntection ไปยัง Application Server เพียงจำนวนเล็กน้อยเท่านั้น ทำให้ Server สามารถรองรับ User ได้จำนวนมากขึ้น

- [x] ทำ Compression, RAM Caching และ Traffic Shaping ให้แก่ Application

เพื่อให้การใช้งานระบบเครือข่ายเป็นไปอย่างมีประสิทธิภาพสูงสุด Application Delivery Controller จึงสามารถทำ Compression เพื่อบีบอัดไฟล์ต่างๆ ที่จะมีการส่งให้กับผู้ใช้งานเพื่อลด Network Traffic ได้โดยตรง รวมถึงยังช่วยทำ Caching บน RAM ของ Application Delivery Controller โดยตรง เพื่อลดจำนวนการ Request ที่ส่งไปยัง Application Server และลด Latency ในการตอบสนอง User ไปพร้อมๆ กัน อีกทั้งยังสามารถกำหนดนโยบาย Traffic Shaping เพื่อทำ QoS สำหรับ Application ต่างๆ ให้แตกต่างกันได้อีกด้วย

- [x] เพิ่มการรักษาความปลอดภัยให้แก่ Application

ความปลอดภัยก็เป็นอีกปัจจัยที่สำคัญของ Application ดังนั้น Application Delivery Controller จึงมักจะเสริมความสามารถทางด้านความปลอดภัยอย่างหลากหลาย ไม่ว่าจะเป็นการทำ Hardened OS เพื่อให้ยากต่อการถูกโจมตี, การกำหนด Firewall/ACL Policy, การป้องกันการโจมตีแบบ TCP syn-flood, การป้องกัน DoS และ DDoS, การทำ URL Filtering และการทำ Web Application Firewall, การป้องกัน SQL Injection, การบริหารจัดการ Certificate และการตรวจสอบ Log การเข้าถึงต่างๆ ได้อย่างครบถ้วน ทำให้ Application ทั้งหมดถูกปกป้องจากการโจมตีรูปแบบต่างๆ ด้วย Application Delivery Controller ไว้อีกชั้นหนึ่งนอกเหนือจาก Firewall และ IPS

- [x] รองรับการทำงานภายใน Cloud Infrastructure

สำหรับการติดตั้ง Application Delivery Controller เพื่อใช้งานในระบบเครือข่ายขนาดใหญ่ เช่นระบบ Cloud การบริหารจัดการก็จะสามารถทำงานร่วมกับระบบ Cloud ได้ทันที เพื่อทำการ Automation การตั้งค่าต่างๆ และรองรับการสร้าง Workflow เพื่อให้การบริหารจัดการเป็นไปได้อย่างรวดเร็วยิ่งขึ้น
