---
layout: post
title: "Backpropagation 수식으로 이해하기"
category: Deep learning
date: 2018-12-30
author: Yangseung
---

<hr>
<p>Backpropagation을 하는 이유, backpropagation의 개념을 알아보고 직접 수식을 전개하면서 이해해 보도록 하겠습니다.
<hr>

<h3>Backpropagation을 하는 이유</h3>
<p>공학자들은 더 복잡한 문제를 풀기 위해 network를 깊게하고 싶어했지만 그렇게 할 수 없었습니다. (network가 deep할수록 non-linear activation function이 많이 사용되고 parameter수도 증가하여 더 높은 차원을 표현 가능)</p>
<p>그 이유는 network를 깊게 만들게 되면 layer들이 많아지게 되고 중간의 layer들이 output에 어떻게, 얼마나 영향을 미치는지 알 수가 없기 때문입니다.  
  hidden unit output이 어떠한 방향으로 가야 network가 정답에 가까워지는지 알 수 없었기 때문에 weight parameter들을 옳은 방향으로 update를 할 수가 없고 원하는 문제를 해결할 수 없게 됩니다. 이를 해결한 방법이 바로 backpropagation입니다.
<p>Backpropagation algorithm은 hidden unit output들이 어떠한 방향으로 가야하는지 즉, hidden unit의 weigth들을 어떠한 방향으로 update를 해주어야 하는지에 대한 방법을 제시해줍니다.</p>
<hr>
  
