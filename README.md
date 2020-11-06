# Matlab avgTemp
Matlab을 사용하여 한 지역의 평균 기온을 구하는 코드를 작성해보았습니다.
```
function T_avg = avgTemp(T_mean, T_peak, t_start, t_end)
```
T_mean: 평균 연간 기온

T_peak: peak 기온

t_start: 시작하는 날(1부터 시작)

t_end: 끝나는 날
```
omega = 2*pi/365; 
```
연간 변화량에 대한 주파수 
```
t = t_start:t_end;
```
온도를 측정한 시간 t의 범위를  t_start에서 t_end까지로 정해줍니다.
```
t_peak = 205;
```
```
T = T_mean+(T_peak-T_mean)*cos(omega*(t-t_peak));
```
연간 기온을 approximation 할 수 있는 식을 작성해줍니다.
```
T_avg = mean(T);
```
mean()을 이용하여 T의 평균을 구해줍니다.

