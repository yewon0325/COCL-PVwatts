# COCL에서 사용한 딥러닝에 대해 조사
PyTorch의 핵심 모듈과 Carbon_Track 모듈을 사용하여 학습 중에 탄소 배출량을 추적한다.

PyTorch란?<br/>
PyTorch는 Python 기반의 과학 연산 패키지로 다음 두 가지 목적으로 제공한다.<br/>
1. GPU 및 다른 가속기의 성능을 사용하기 위한 NumPy의 대체제 제공<br/>
2. 신경망 구현에 유용한 자동 미분(automatic differntiation) 라이브러리 제공<br/>

PyTorch 패키지<br/>
torch: 강력한 GPU 지원 기능을 갖춘 Numpy와 같은 라이브러리<br/>
torch.nn: 최고의 유연성을 위해 설게된 자동 그래프와 깊이 통합된 신경 네트워크 라이브러리<br/>
torch.autogradad: Torch에서 모든 차별화된 Tensor 작업을 지원하는 테이프 기반 자동 미분화 라이브러리<br/>
torch.optim: SGD, RMSProp, LBFGS, Adam등과 같은 표준 최적화 방법으로 torch.nn과 함께 사용되는 최적화 패키지<br/>
torch.utils: 편의를 위해 DataLoader, Trainer 및 기타 유틸리티 기능<br/>
*'datasets 및 transforms는 PyTorch에서 제공하는 데이터셋 및 전처리 도구<br/><br/>

신경망은 torch.nn 패키지를 사용하여 생성할 수 있다<br/>
![image](https://github.com/yewon0325/COCL-PVwatts/assets/147733678/f4953186-a7fb-4b9d-b735-73ef9644885a)
<br/>
신경망의 일반적인 학습 과정
학습 가능한 매개변수(또는 가중치(weight))를 갖는 신경망을 정의한다.<br/>
데이터셋(dataset) 입력을 반복한다.<br/>
입력을 신경망에서 전파(process)한다.<br/>
손실(loss; 출력이 정답으로부터 얼마나 떨어져 있는지)을 계산한다.<br/>
변화도(gradient)를 신경망의 매개변수들에 역으로 전파한다.<br/>
신경망의 가중치를 갱신한다.<br/>
일반적으로 다음과 같은 간단한 규칙을 사용: 새로운 가중치(weight) = 가중치(weight) - 학습률(learning rate) * 변화도(gradient)<br/>



