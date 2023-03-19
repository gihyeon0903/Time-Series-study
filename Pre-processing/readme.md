### 시계열 데이터 기초

> - Fourier Transform<br>
임의의 입력 신호를 다양한 주파수를 가지는 주기함수들의 합으로 표현하는 것
> - FFT(Fast Fourier Transform)<br>
DFT를 빠르게 수행하는 효율적인 알고리즘<br>
시간복잡도 DFT(n^2) / FFT(nlogn)
> - Sampling rate = Sampling Freq<br>
연속된 신호에서 얻어진 초단 sampling 횟수를 의미 / 단위 Hz
> - Nyquist Frequency (fn)<br>
FFT에 의해 결정될 수 있는 이론상 최대 주파수를 의미(fn = fs/2)
> - Block length/size or Window length/size<br>
FFT를 수행할 사이즈
> - Frequency resolution (df)<br>
두 측정 결과 간의 주파수 간격을 나타냄.(df = fs/BL)
> - Windowing
FFT는 DFT로 유한한 길이를 가지는 신호에 대한 변환이기 때문에 비주기적이며 주파수 영역에서 에너지가 퍼지는 “누설leakage”현상이 나타나게 됨<br>
window함수를 이용하여 불연속점을 채워 비주기 신호를 마치 주기적이며 연속적인 신호로 바꿔줌<br>

다양한 window 함수<br>
1. Flat Top       진폭의 정밀도를 높일 때 사용, 단일 주파수의 정밀 진폭 측정, 센서 교정시 사용<br>
2. Hanning        정상적인 연속 데이터 분석 시 사용, 일반적 진동 해석에 적용, 진폭치는 정확하지 않아도 정확한 진동수를 구별할 때<br><br>
3. Rectangular    시간 T안에서 현상이 종료되는 과도 데이터, Order Tracking 분석에 사용, 크기가 같은 근접 주파수를 분리하여 측정할 때 사용<br>
4. Exponential    다소 긴 시간 내에 현상이 종료되는 과도 데이터, Impulse Test 시 사용<br>
5. Kaiser-Bessel  크기가 다른 근접 주파수를 분리해석할 때 사용<br>
