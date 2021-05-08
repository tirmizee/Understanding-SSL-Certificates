# Understanding-SSL-Certificates


### สาเหตที่ใบรับรอง certificate ไม่ถูกต้องอาจจะเป็นไปได้หลายอย่าง
- #### ใบรับรองหมดอายุ (Expired certificate)
- #### ใบรับรองที่ลงนามด้วยตันเอง (Self-signed certificate)
- #### ข้อมูลโฮสต์ในใบรับรองไม่ถูกต้อง (Wrong host information in certificates)
- #### ใบรับรองถูกเพิกถอน (Revoked certificate)
- #### CA ไม่น่าเชื่อถือ
### Disable or bypass SSL certificate checking (ปิดใช้งานหรือข้ามการตรวจสอบ SSL certificate)
 เราจะ disable หรือ bypass การตรวจอสบ SSL certificate โดยการเชื่อถือใบรับรองทุกประเภท

### Reference

- https://support.code42.com/Administrator/6/Configuring/Install_a_CA-signed_SSL_certificate_for_HTTPS_console_access
