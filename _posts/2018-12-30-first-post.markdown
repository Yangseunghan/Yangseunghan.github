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

<p>공학자들은 더 복잡한 문제를 풀기 위해 network를 깊게하고 싶어했지만 그렇게 할 수 없었습니다.<br/> (network가 deep할수록 non-linear activation function이 많이 사용되고 parameter수도 증가하여 더 높은 차원을 표현 가능)</p>

<p>그 이유는 network를 깊게 만들게 되면 layer들이 많아지게 되고 중간의 layer들이 output에 어떻게, 얼마나 영향을 미치는지 알 수가 없기 때문입니다. <br/> hidden unit output이 어떠한 방향으로 가야 network가 정답에 가까워지는지 알 수 없었기 때문에 weight parameter들을 옳은 방향으로 update를 할 수가 없고 원하는 문제를 해결할 수 없게 됩니다. 이를 해결한 방법이 바로 backpropagation입니다.</p>
  
<p>Backpropagation algorithm은 hidden unit output들이 어떠한 방향으로 가야하는지 즉, hidden unit의 weigth들을 어떠한 방향으로 update를 해주어야 하는지에 대한 방법을 제시해줍니다.</p>

<hr>
  
<h3>Backpropagation이란?</h3>
<p>Backpropagation 이름은 정말 거창하지만 알고 보면 별거 없습니다. 왜 이걸 알아내는데 그렇게 오래 걸렸을까 하는 의문이 들 정도로..</p>

<p>Supervised learning에서 objective function
<img src="/post_images/1_1.png" width="10px", height="10px"></p>

<p>objective function을 최소화 하는 즉 이 training error를 최소화 하는 방향으로 모든 parameter를 계속해서 update해주어야 합니다.<br/>
(Deep learning에서는 gradient descent방법을 사용. objective function이 최소가 되게하는 parameter들을 미분과 연립방정식으로 찾는게 아닌 objective function의 값이 줄어드는 방향으로 계속해서 parameter들을 update.)<br/></p>

<p>그러기 위해서는 각 parameter에 대한 objective function의 변화량을 알아야 하고, 아래와 같이 구할 수 있습니다.<br/>
<p align = "center"><img src="/post_images/1_2.png"></p></p>

<p>Objective function을 모든 parameter에 대해 편미분을 해줌으로써 parameter가 objective function에 어떠한 영향을 미쳤는지 알 수 있고 gradient방향 반대로 parameter들을 update하여 objective function을 최소화 할 수 있습니다.<br/>
<p align = "center"><img src="/post_images/1_3.png"></p></p>

<hr>

<h3>수식으로 전개하여 이해하기</h3>
<p>먼저 아래표와 같은 상황에서 수식을 전개한 후 일반화해서 생각해보도록 하겠습니다.</p>
<table cellspacing="0" cellpadding="0">
  <tr>
    <th>Input i </th><th>Hidden j </th><th>Output k </th><th> J(w)</th>
  </tr>
  <tr>
    <td>1 </td><td>1 </td><td>1 </td><td>MSE </td>
  </tr>
</table>

<ul>
  <li>Hidden to output weight</li>
  <p>Hidden layer에서 output layer로 feed forward 할 때 사용되는 parameter가 objective function에 어떠한 영향을 미치는지 살펴보겠습니다.</br>
  아래와 같은 weight에 대한 편미분의 값을 알아내는게 목표입니다.</p>
  <p align="center"><img src="/post_images/1_4.png"></p>
  <p>그러기 위해서는 먼저 feed forward식들을 알아야 하는데 다음과 같습니다.</br>
  우선 아래와 같이 쓰기로 약속을 하고, objective function까지의 식을 전개해보도록 하겠습니다.</p>
  <p align="center"><img src="/post_images/1_5.png"></p>
  <p>bias는 일단 무시한채 진행하였습니다. width는 각각 n, d, c로 정하였습니다.
  <p align="center"><img src="/post_images/1_6.png"></p>
  <p align="center"><img src="/post_images/1_7.png"></p>
  <p>Objective function은 MSE로 정하였고 아래와 같습니다.</p>
  <p align="center"><img src="/post_images/1_8.png"></p>
  <p>이제 본론으로 돌아와서 parameter의 weight들이 objective function에 얼마나 영향을 미치는지 알아 볼 것입니다.</p>
  

  <li>Input to hidden weight</li>
  
</ul>
