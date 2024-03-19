---
title: 'simple org tables'
date: 2024-01-16T20:38:00.005-05:00
draft: false
url: /2024/01/simple-org-tables.html
tags: 
- emacs
---

 simple org table addition

  

| item      | price |

|-----------+-------|

| hotdog    |     1 |

| hamburger |     1 |

| total     |     2 |

#+TBLFM: @4$2=vsum(@2$2..@3$2)

  

\- control c \* to re-evaluate

\- control c = to enter a formula