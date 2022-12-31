---
author: snowmang1
title: {{ replace .Name "-" " " | title }}
date: {{ .Date }}
tag: ["HERE"]
series:
    - HERE
math: true
draft: true
description: check for Katex integration
---

{{ partial "math.html" . }}

<!---------------------- Body ---------------------->
