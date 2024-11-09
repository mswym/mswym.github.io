---
layout:     post
title:      Early color processing, PCA of LMS responses
date:       2024-11-08 21:00:00 +0900
summary:    Buchsbaum & Gottshalk (1983) 
categories: color
---

この記事では，以下のBuchsbaum & Gottshalk (1983)の論文について紹介する．

- Buchsbaum, G., & Gottschalk, A. (1983). Trichromacy, opponent colours coding and optimum colour information transmission in the retina. Proceedings of the Royal Society of London. Series B. Biological Sciences, 220(1218), 89–113.

Buchsbaum & Gottshalk (1983)では，視覚系のRGCやLGNにおける錐体拮抗型細胞の機能的意義について，情報処理の効率性の観点から解析をしている．具体的には，L・M・S錐体の分光感度を持つ仮想のセンサが無作為な光刺激を受容した際に，その信号の主成分分析をした固有ベクトルが錐体拮抗型応答と対応することを示した．

図1は，L・M・S錐体の波長に対する感度を示した関数であり，L錐体とM錐体の応答関数は非常に近いことが読み取れる（）．


これらの各錐体の感度から，錐体応答は以下の式で計算することができる．論文中では，L・M・S錐体の応答関数をR(λ)，G(λ)，B(λ)と表記しているが，画像処理で用いられるRGBとの区別からここでは，L(λ)，M(λ)，S(λ)と表記する．
