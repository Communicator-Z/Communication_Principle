###### 	This section is mainly about some basic matlab codes, which include plot continuous signal, stem discrete signal, differential and integral.

- plot function graph

  ```matlab
  t = -1:0.01:1;
  f1 = 2*exp(3*abs(t));
  subplot(2,2,1)
  plot(t,f1)
  xlabel('t(sec)')
  ylabel('f1')
  title('2exp(3|t|)');
  grid;
  subplot(2,2,2)
  f2 = 2*exp(-3*abs(t));
  plot(t,f2)
  xlabel('t(sec)')
  ylabel('f2')
  title('2exp(-3|t|)');
  grid;
  subplot(2,2,3)
  f3 = sin(6*pi*t)+cos(10*pi*t);
  plot(t,f3)
  xlabel('t(sec)')
  ylabel('f3')
  title('sin(6*pi*t)+cos(10*pi*t)');
  grid;
  subplot(2,2,4)
  f4 = abs(t).*cos(10*pi*t);
  plot(t,f4)
  xlabel('t(sec)')
  ylabel('f4')
  title('|t|*cos(10*pi*t)');
  grid;
  ```

  The result graph is as follows:

  <img src="E:\各种学习资料\研究生阶段\MATLAB\matlab_personal_practice\Communicaiton_principle\determinate signal\priodic signal\signal_and_system\continuous_time_signal\1.jpg" style="zoom: 50%;" />

- Use function to generate graph:

  ```matlab
  function y = f(t)
  %F 此处显示有关此函数的摘要
  %   此处显示详细说明
  y = t*exp(-cos(t))/(1+t^2);
  end
  ```

  ```matlab
  t = 0:0.1:50;
  N = length(t);
  y = zeros(1,N);
  for n = 1:N
      y(n) = f(t(n));
  end
  figure
  plot(t,y);
  grid
  xlabel('t')
  ylabel('y')
  title('Function f(t)');
  ```

  The result graph is as follows:

  <img src="E:\各种学习资料\研究生阶段\MATLAB\matlab_personal_practice\Communicaiton_principle\determinate signal\priodic signal\signal_and_system\continuous_time_signal\2.jpg" style="zoom:50%;" />

  

