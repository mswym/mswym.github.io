---
layout:     post
title:      Early color processing
date:       2024-10-05 21:00:00 +0900
summary:    Introduction to efficient color coding 
categories: color
---


網膜上のL錐体，M錐体，S錐体の３種類の光センサで実世界の波長光を受容した後，網膜神経節細胞(retinal ganglion cell, RGC)や外側膝状体(lateral geniculate nucleus,LGN)では，３つのセンサ信号を加算・減算によって組み合わせた表現に変換し，その情報を大脳皮質へと伝達する．具体的には，輝度と色の表現をする細胞が確認されており，輝度チャネルとしてはL錐体応答とM錐体応答とを加算した表現(L+M)が知られる．そして，色チャネルとしては2種類あり，ひとつは，L錐体応答とM錐体応答の差分を表現するチャネル(L-M)で，もうひとつは，S錐体応答とLおよびM錐体応答の和との差分を表現するチャネルが知られる(S-(L+M))．L錐体，M錐体，S錐体それぞれが特定のカテゴリ色と完全に対応しているわけではないため，色名で軸を表現することは厳密には正しくはないが，無彩色を0とした場合のL-M軸は赤っぽい色から緑っぽい色への変化を表現し，S-(L+M)は青っぽい色から黄色っぽい色への変化を表現する．余談になるが，色名としての反対色（赤-緑，黄-青）と神経生理学的基盤については現在でも議論が続いていて，以下の近年のレビュー論文では色名としての反対色に明確な神経生理学的基盤が見られないことについて議論がされている(Conway et al., 2023)．
<br><br>

- Conway, B. R., Malik-Moraleda, S., & Gibson, E. (2023). Color appearance and the end of Hering’s Opponent-Colors Theory. Trends in Cognitive Sciences.

この記事では，輝度チャネルと２つの色チャネルの神経生理学的基盤については詳しく述べない．その代わり，センサ信号での光受容の次のステップとして行われる処理の機能的意義について，いくつかの研究を概観しながら考察していく．具体的には，情報処理の効率性という観点からセンサ信号の変換過程について議論する．
<br><br>

はじめに，視覚系が行う輝度・色チャネルの分解が，L・M・S錐体の分光感度を用いてセンシングした信号の主成分分析の結果とよく対応することを，以下の２つの論文を概観しながら述べる(Buchsbaum & Gottschalk, 1983; Ruderman et al., 1998)．このことは，RGCやLGNにおける信号の変換過程が，冗長な錐体信号の無相関化して効率的に処理するという機能的意義を持つということを示唆している．
<br><br>

- Buchsbaum, G., & Gottschalk, A. (1983). Trichromacy, opponent colours coding and optimum colour information transmission in the retina. Proceedings of the Royal Society of London. Series B. Biological Sciences, 220(1218), 89–113.

- Ruderman, D. L., Cronin, T. W., & Chiao, C.-C. (1998). Statistics of cone responses to natural images: implications for visual coding. JOSA A, 15(8), 2036–2045.

次に，この段階の信号の変換過程がある程度効率的ではあるものの，自然環境下で観察する画像の効率的な分解ということを考慮すると，あまり効率的とは言えないということについて議論する．具体的には，Lee et al. (2022) の研究を紹介し，自然情景画像においてL・M・S錐体応答の独立成分分析をした結果の色軸は，視覚系の錐体拮抗応答とは若干異なることを議論する．さらに，輝度チャネルが色チャネルと分離する点についても，自然環境下で観察する物体については，効率的な分離ではないことを議論する．この点はあまり多くの先行研究で議論されていないが，光学的に複雑な多様な質感を考慮すると，自然物体画像の輝度と色の相関は非常に高い（冗長である・効率的な表象ではない）ことについて議論していく(Fleming et al., 2005; Nishida, 2010; Liao, Sawayama, & Xiao, 2022)．ここでの議論は，視覚系が自然環境を効率的に処理することをめざすという観点を否定するものではない．RGCやLGNでの効率化が自然環境下における効率的な情報処理として十分でないことに注意を向けることで，どのような効率的な処理があり得るかという将来的な検討の方向を提案する目的で議論をしていく．
<br><br>

- Fleming, R. W., & Bülthoff, H. H. (2005). Low-level image cues in the perception of translucent materials. ACM Transactions on Applied Perception (TAP), 2(3), 346-382.

- Nishida, S. (July, 2010). Perception of colorful natural scenes, Asia-Pacific Conference on Vision, Taipei (Taiwan).

- Liao, C., Sawayama, M., & Xiao, B. (2022). Crystal or jelly? Effect of color on the perception of translucent materials with photographs of real-world objects. Journal of Vision, 22(2), 6-6.
