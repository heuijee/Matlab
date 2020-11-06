# Matlab avgTemp
Matlab을 사용하여 한 지역의 평균 기온을 구하는 코드를 작성해보았습니다.

  function T_avg = avgTemp(T_mean, T_peak, t_start, t_end)

T_mean: 평균 연간 기온

T_peak: peak 기온

t_start: 시작하는 날(1부터 시작)

t_end: 끝나는 날

omega = 2*pi/365; 

연간 변화량에 대한 주파수 

t = t_start:t_end;

t_peak = 205;


T = T_mean+(T_peak-T_mean)*cos(omega*(t-t_peak));

T_avg = mean(T);

end

