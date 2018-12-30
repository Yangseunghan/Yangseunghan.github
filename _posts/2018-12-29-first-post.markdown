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
<p>공학자들은 더 잡한 문제를 풀기 위해 network를 깊게하고 싶어했지만 그렇게 할 수 없었습니다.  
(network가 deep할수록 non-linear activation function이 많이 사용되고 parameter수도 증가하여 더 높은 차원을 표현 가능)  
그 이유는 network를 깊게 만들면 hidden unit output이 어떠한 방향으로 가야 network가 정답에 가까워지는지 알 수 없었기 때문입니다.  
  hidden unit output들이 어떠한 방향으로 가야하는지 즉, hidden unit의 weigth들을 어떠한 방향으로 update를 해주어야 하는지에 대한 방법이 바로 Backpropagation방법입니다.
  
  <hr>
  
