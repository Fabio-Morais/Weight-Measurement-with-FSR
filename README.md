# Weight Measurement with FSR

----

##### The main goal was to project and implement a weight measurement system based on FSR (Force Sensing Resistor) technology. For that, we would have to develop an electronic circuit for signal conditioning and a virtual instrument to acquire the signals from a data acquisition board. Afterwards we characterized both static and dynamic behavior of the FSR sensors to calibrate them and to have a reliable representation of the applied pressure. 

----


Foram colocados diversos pesos de modo a obter uma caracterização adequada e completa do sistema de medição. Sem pressão tivemos um valor de resistência na ordem dos Mega Ohms, sendo que o ultímetro apresentou o seu valor máximo de 40MΩ.
Reparámos também que o peso mínimo de deteção rondava os cerca de 250g sendo que a resistência assumia logo o patamar de alguns kΩ.

<p align="center">
  <img src="https://user-images.githubusercontent.com/35969631/52054211-af980680-2553-11e9-923c-a6747dfe1e36.png" width="500" height="270">
</p>

Decidimos utilizar um divisor resistivo para poder ter uma queda de tensão correspondente a cada patamar de peso e através de um amplificador comparador foi possível desenvolver um sistema que tem uma gama dinâmica de medições compreendido entre -10V e 10V consoante vai tendo mais peso a ser aplicado. Foi utilizado ainda à saída um filtro passa baixo para reduzir ruído eletromagnético induzido pelas lâmpadas e equipamentos circundantes. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/35969631/52054711-50d38c80-2555-11e9-8121-0b529bcb497c.png" >
</p>

Com este par de resistor / capacitor conseguimos produzir um filtro passa baixo que teoricamente atenua frequencias a partir de 0,72Hz o que é ótimo para o que queremos. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/35969631/52054628-110ca500-2555-11e9-8e3b-a15b2804c292.png" width="430" height="270">
</p>

Paralelamente começou a ser desenvolvido o instrumento virtual na plataforma *Labview*. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/35969631/52130919-6e772380-2633-11e9-976a-7ee7b0dc64e7.png" width="430" height="270">
</p>

Através de 4 mostradores gráficos, 4 mostradores de escala, 4 mostradores numéricos e uma representação por LEDs dos sensores pressionados é possível determinar em tempo real a tensão aplicada. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/35969631/52131036-b8f8a000-2633-11e9-9b00-3aa24fbc42ca.png" width="430" height="270">
</p>

O diagrama de blocos em Labview está representada na figura seguinte

<p align="center">
  <img src="https://user-images.githubusercontent.com/35969631/52131179-0b39c100-2634-11e9-9867-a7358a6cb488.png" width="630" height="560">
</p>


**Relatorio do trabalho [aqui](https://github.com/fabiouds/Weight-Measurement-with-FSR/blob/master/Report.pdf)**
