# Stock-volatility-prediction-based-on-multiple-LSTM-models
## Introduction
Stock volatility can reflect the volatility of the price and the future risk of the assets, and historical volatility is an important measure of stock volatility. The scientific and accurate prediction model of stock historical volatility is of great significance for the estimation of the future asset risk situation and the maintenance of the smooth operation of the financial market. Classical time series models have been widely used. <br>In order to obtain more accurate prediction models, this report proposes the stock historical volatility prediction model composed of *`two LSTM neural networks and two fully connected layers`*, so as to improve the ability of the model to effectively capture the complex nonlinear relationship in the time series prediction task.
## Core Model
### LSTM model of two fully connected layers
The neural network structure we take consists of two fully connected layers and two LSTM layers. In order to accelerate the convergence speed, enhance the model stability, and improve the generalization ability, we add the batch standardization (BN) layer before the LSTM network of each layer. To improve the ability of the model to express non-linear sequences, we added the full connection (Dense) layer before and at the end of the LSTM network. The specific structure of the model is as follows:<br><br><br>
![图片1](https://github.com/opdpjfj/Stock-volatility-prediction-based-on-multiple-LSTM-models/assets/125139348/fa903923-8004-4732-8e4a-b1daebfe0a23)
## Model Prediction
After model training, we predicted the historical stock volatility of the next ten time steps according to the model parameters, and then rever-normalized the predicted value of the features to get the predicted result. The prediction data and effect of the model are shown as follows:<br><br><br>
<table class="MsoTableGrid" border="1" cellspacing="0" style="border-collapse:collapse;width:482.1500pt;margin-left:-41.5500pt;
border:none;mso-border-left-alt:0.5000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;
mso-border-right-alt:0.5000pt solid windowtext;mso-border-bottom-alt:0.5000pt solid windowtext;mso-border-insideh:0.5000pt solid windowtext;
mso-border-insidev:0.5000pt solid windowtext;mso-padding-alt:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;"><tbody><tr><td width="103" valign="top" style="width:51.6500pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">时间步</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">1</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">2</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">3</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">4</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">5</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">6</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">7</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">8</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">9</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="112" valign="top" style="width:56.1000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">10</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td></tr><tr><td width="103" valign="top" style="width:51.6500pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">预测值</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">394</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.01</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">3359</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">13317</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">139</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">12879</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">12583</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">12271</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">11974</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.012950</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="112" valign="top" style="width:56.1000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.0</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><font face="Calibri Light">11705</font></span><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td></tr><tr><td width="103" valign="top" style="width:51.6500pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><font face="宋体">实际值</font></span><span style="font-family:宋体;letter-spacing:-0.1000pt;font-size:12.0000pt;
mso-font-kerning:1.0000pt;position:relative;top:-1.0000pt;
mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013124</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013173</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013323</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013156</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.012638</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013058</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013418</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013200</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="83" valign="top" style="width:41.6000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.013227</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td><td width="112" valign="top" style="width:56.1000pt;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:1.0000pt solid windowtext;
mso-border-left-alt:0.5000pt solid windowtext;border-right:1.0000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;"><p class="MsoNormal" style="margin-top:4.9000pt;line-height:15.3000pt;mso-line-height-rule:exactly;"><span style="font-family:'Calibri Light';mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;">0.009707</span><span style="font-family:宋体;mso-ascii-font-family:'Calibri Light';mso-hansi-font-family:'Calibri Light';
letter-spacing:-0.1000pt;font-size:7.5000pt;mso-font-kerning:1.0000pt;
position:relative;top:-1.0000pt;mso-text-raise:1.0000pt;"><o:p></o:p></span></p></td></tr></tbody></table>



<br><br><br>
![图片2](https://github.com/opdpjfj/Stock-volatility-prediction-based-on-multiple-LSTM-models/assets/125139348/bb6e35b1-f116-4664-9c85-5627d989552b)
