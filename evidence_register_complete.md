# LAB 2 EVIDENCE REGISTER
# File Upload and Command Execution Security Assessment
# CIP-A104 — Offensive Security Operations I

---

## E-1: DVWA Security Level
- **Description:** DVWA security page showing level set to "Impossible"
- **File:** E-1_DVWA_security_level.jpg
- **Purpose:** Document baseline security configuration

---

## E-2: DVWA File Upload Interface
- **Description:** DVWA file upload page showing upload form
- **File:** E-2_DVWA_file_upload_Interface.jpg
- **URL:** http://192.168.56.107/dvwa/vulnerabilities/upload/
- **Purpose:** Document upload interface before testing

---

## E-3: Selected Upload File
- **Description:** lab2-upload-marker.png selected for upload
- **File:** E-3_Selected_upload_file.jpg
- **File:** lab2-upload-marker.png
- **Purpose:** Show file selected before upload

---

## E-4: Normal Upload Response
- **Description:** Upload success message
- **File:** E-4_Normal_upload_response.jpg
- **Result:** "8ef52f3e35c533c8291309deec5fcdec.png successfully uploaded!"
- **Purpose:** Document successful normal upload

---

## E-5: Browser Retrieval
- **Description:** Accessing uploaded file via browser
- **File:** E-5_DVWA_browser_retrieval.jpg
- **URL:** http://192.168.56.107/dvwa/hackable/uploads/8ef52f3e35c533c8291309deec5fcdec.png
- **Result:** Image displayed successfully
- **Purpose:** Prove file is web-accessible

---

## E-6: HTTP Retrieval (curl)
- **Description:** curl -I request showing 200 OK
- **File:** E-6_DVWA_http_retrieval.jpg
- **Status:** HTTP/1.1 200 OK
- **Content-Type:** image/png
- **Content-Length:** 99 bytes
- **Purpose:** Confirm file accessible via HTTP

---

## E-7: Retrieved Properties
- **Description:** file, stat, sha256sum of retrieved file
- **File:** E-7_DVWA_Retrieved_properties.jpg
- **Type:** image/png
- **Size:** 99 bytes
- **SHA-256:** b584d71ebf1b94e6a676272fa325851c735639354f500482337d0151dc5c017
- **Purpose:** Document retrieved file properties

---

## E-8: Integrity Comparison
- **Description:** SHA-256 comparison between original and retrieved
- **File:** E-8_DVWA_integrity_comparision.jpg
- **Original SHA-256:** 4ded5810edc347f756bda4743eedc8d814281ba05262e55713a9ccb177cf5226
- **Retrieved SHA-256:** b584d71ebf1b94e6a676272fa325851c735639354f500482337d0151dc5c017
- **Result:** Different hashes (file was renamed)
- **Purpose:** Prove file was stored with different name

---

## E-9: Mismatch Test
- **Description:** Upload of file with mismatched extension
- **File:** E-9_DVWA_mismatch_test.jpg
- **Result:** POST request/response captured
- **Status:** 200 OK
- **Purpose:** Document server-side validation testing

---

## E-10: Mutillidae Upload Page
- **Description:** Mutillidae file upload interface
- **File:** E-10_Mutillidae_upload_page.jpg
- **URL:** http://192.168.56.107:8081/index.php?page=upload-file.php
- **Purpose:** Document Mutillidae upload interface

---

## E-11: Mutillidae TXT Upload
- **Description:** Upload of lab2-upload-marker.txt
- **File:** E-11_Mutillidae_txt_upload_success.png
- **Result:** Upload successful → /tmp/lab2-upload-marker.txt
- **SHA-256:** d351bb9cf91b74f3b2bb893b4f4743f900ed930deccbcf2ffc4e9f73ab731452
- **Purpose:** Document normal upload behavior

---

## E-12: Mutillidae PHP Upload (Mismatch)
- **Description:** Upload of lab2-upload-marker.php
- **File:** E-12_mutillidae_php_upload.png
- **SHA-256:** 5aa3b559616ba61e701f1c6e5c2e6813f30cad9ba54174efe55a24f6a3a46513
- **File:** E-12_mutillidae_php_upload.png
- **Result:** Upload successful, no validation performed
- **Purpose:** Prove no server-side validation exists

---

## E-13: Mutillidae DNS Baseline
- **Description:** Normal DNS lookup for 127.0.0.1
- **File:** E-13_mutillidae_dns_baseline.png
- **Result:** DNS query response (NXDOMAIN)
- **Purpose:** Document normal command behavior

---

## E-14: Mutillidae Command Injection
- **Description:** Command injection with "127.0.0.1; whoami"
- **File:** E-14_mutillidae_command_injection.png
- **Result:** Output shows "www-data"
- **Purpose:** Prove command injection vulnerability

---

## E-15: Mutillidae Secure Mode
- **Description:** Secure mode blocking malicious characters
- **File:** E-15_mutillidae_secure_mode.png
- **Security Level:** 5 (Secure)
- **Result:** "Malicious characters are not allowed"
- **Purpose:** Compare insecure vs secure mode

---

## E-16: DVWA Database Reset	
- **Description:** DVWA Database Reset
- **File:** E-16_DVWA_Database_Reset.png

---

## E-17: Mutillidae Database Reset
- **Description:** Mutillidae Database Reset
- **File:** E-17_Mutillidae_Database_Reset.png

---

## FILE HASHES SUMMARY

| File | SHA-256 |
|------|---------|
| lab2-upload-marker.png (original) | 4ded5810edc347f756bda4743eedc8d814281ba05262e55713a9ccb177cf5226 |
| lab2-upload-marker.png (retrieved) | b584d71ebf1b94e6a676272fa325851c735639354f500482337d0151dc5c017 |
| lab2-upload-marker.txt | d351bb9cf91b74f3b2bb893b4f4743f900ed930deccbcf2ffc4e9f73ab731452 |
| lab2-upload-marker.html | aee76ebeda877228a62445e61534461b0be2f9fca5b2c709929c042ace060833 |
| lab2-upload-marker.php | 5aa3b559616ba61e701f1c6e5c2e6813f30cad9ba54174efe55a24f6a3a46513
