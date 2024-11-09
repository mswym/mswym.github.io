---
layout:     post
title:      Early color processing, PCA of LMS responses
date:       2024-11-08 21:00:00 +0900
summary:    Buchsbaum & Gottshalk (1983) 
categories: color
---

この記事では，以下のBuchsbaum & Gottshalk (1983)の論文について紹介する．
<br><br>
- Buchsbaum, G., & Gottschalk, A. (1983). Trichromacy, opponent colours coding and optimum colour information transmission in the retina. Proceedings of the Royal Society of London. Series B. Biological Sciences, 220(1218), 89–113.

Buchsbaum & Gottshalk (1983)では，視覚系のRGCやLGNにおける錐体拮抗型細胞の機能的意義について，情報処理の効率性の観点から解析をしている．具体的には，L・M・S錐体の分光感度を持つ仮想のセンサが無作為な光刺激を受容した際に，その信号の主成分分析をした固有ベクトルが錐体拮抗型応答と対応することを示した．
<br><br>

論文図2は，L・M・S錐体の波長に対する感度を示した関数であり（Vos & Walraven, 1971），L錐体とM錐体の応答関数は非常に近いことが読み取れる．論文中では，L・M・S錐体の応答関数を $R(\lambda),G(\lambda),B(\lambda)$ と表記しているが，画像処理で用いられるRGBとの区別からこの記事では， $L(\lambda),M(\lambda),S(\lambda)$ と表記する．
<br><br>
<div align="center" style="margin-bottom:40px">
	<img class="80" src="/images/Buchsbaum_1983_fig2.png" width="60%" alt="Figure 2 of Buchsbaum & Gottshalk, 1983" />
<sub style="display: block; line-height: 1.5em">
	<i> (figure credit:
Buchsbaum & Gottshalk, 1983,
<a href="https://royalsocietypublishing.org/doi/10.1098/rspb.1983.0090" target="_blank">link to paper</a>)</i></sub>
</div>
<br><br>

これらの波長 $\lambda$ に対する各錐体の応答関数 $L(\lambda),M(\lambda),S(\lambda)$ から，錐体応答量 $l,m,s$ は以下の式で計算することができる．
<br><br>

$$
l = \int I(\lambda) L(\lambda) d\lambda, \quad m = \int I(\lambda) M(\lambda) d\lambda, \quad s = \int I(\lambda) S(\lambda) d\lambda.
$$

ここで， $S(\lambda)$ は入力光の分光強度を意味しており，解析には $N$ 個の無作為な分光分布を持つ入力を用いている．Nx3の入力画像に対して，
