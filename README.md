# PID Betaflight 4.2

<img src="https://raw.githubusercontent.com/wiki/betaflight/betaflight/images/betaflight/bf_logo.png">

En este repositorio iré posteando los consejos para ajustar los PID de **Betaflight 4.2.x**.  
Recordad que para usar esta versión de Betaflight es necesario el **Betaflight Configurator version 10.7.0**.  
El uso de esta información queda bajo la responsabilidad de cada usuario.

En la version 4.2 tenemos los **Sliders**, comunmente llamadas "barritas" de los PID.      
Nos ayudan a mantener la proporcionalidad diseñada por los creadores de Betaflight en los valores de los PIDs.   
Para empezar tambien es recomendable deshabilitar el **modo experto** para reducir el rango de los sliders.  
Por defecto tienen todos el valor de 1. Tambien podemos editar los valores de forma individual, en ese caso los Sliders desaparecerán.   

La comunidad de betaflight nos comparte los PID de algunos pilotos y sus quads.  

[PIDs Recomendados por Betaflight]https://github.com/betaflight/betaflight/wiki/Community-Presets

Por ejemplo, el piloto **JJang FPV** nos recomienda estos ajustes para un quad **5" 4S Normal Freestyle** con bateria 4S y Gopro 6/7/8 .    
Este ajuste nos dice que es para una respuesta buena del quad pero suave, para **cinematic, juicy and more**. Eliminando el propwash.

JJang FPV  
Caution: You should activate **'Bidirectional Dshot'** for rpm filter and adjust 'idle_min_rpm' about 70% of dshot_idle_rpm or start with '21'.   

set gyro_lowpass2_hz = 300  
set dyn_notch_width_percent = 0  
set dyn_notch_q = 250  
set dyn_notch_min_hz = 90  
set dyn_notch_max_hz = 515  
set dyn_lpf_gyro_min_hz = 240  
set dyn_lpf_gyro_max_hz = 600  
set min_check = 1020  
set max_check = 1995  
set rc_smoothing_auto_smoothness = 7  
set blackbox_device = NONE  
set min_throttle = 1020  
set dshot_idle_value = 500  
set dshot_bidir = ON  
set use_unsynced_pwm = OFF  
set motor_pwm_protocol = DSHOT300  
set deadband = 2  
set yaw_deadband = 2  
set pid_process_denom = 2  
set gyro_rpm_notch_q = 700  
set dyn_lpf_dterm_min_hz = 84  
set dyn_lpf_dterm_max_hz = 204  
set dyn_lpf_dterm_curve_expo = 7  
set dterm_lowpass2_hz = 180  
set vbat_sag_compensation = 100  
set pid_at_min_throttle = OFF  
set anti_gravity_gain = 3900  
set feedforward_transition = 40  
set iterm_relax_type = GYRO  
set iterm_relax_cutoff = 20    
set yaw_lowpass_hz = 100  
set throttle_boost = 7  
set throttle_boost_cutoff = 25  
set p_pitch = 65  
set i_pitch = 104  
set d_pitch = 58  
set f_pitch = 116  
set p_roll = 60  
set i_roll = 99  
set d_roll = 54  
set f_roll = 109  
set p_yaw = 69  
set i_yaw = 99  
set f_yaw = 109  
set d_min_roll = 35  
set d_min_pitch = 39  
set ff_interpolate_sp = AVERAGED_3  
set ff_spike_limit = 70  
set ff_smooth_factor = 40  
set idle_min_rpm = 21  
set roll_rc_rate = 120  
set pitch_rc_rate = 120  
set yaw_rc_rate = 175  
set roll_expo = 15  
set pitch_expo = 15  
set yaw_expo = 20  
set roll_srate = 72  
set pitch_srate = 75  
set yaw_srate = 41  
set tpa_rate = 70  
set tpa_breakpoint = 1150  
set throttle_limit_type = CLIP  
set throttle_limit_percent = 98  

save  

Ignacio de QuadMx nos pone ejemplos de hacia donde tienden los PIDs generalizados dependiendo de los estilos de vuelo.  
Por ejemplo, estos serian para Freestyle en un quad 5":  
<img src="https://raw.githubusercontent.com/AirbenderFPV/PID-Betaflight-4.2/main/PIDejemploFreestyle.PNG">

El **Master Multiplier** incrementado para contrarestar un poco el peso del quad.   
El **PD Balance** mejora bounceback o situaciones en giros de 180º.  
El **P and D Gain** se mantiene para el propwash.   
El **Stick Response Gain** decrementado para suavizar los movimientos, si haces un freestyle mas agresivo recomiendo dejar el valor por defecto.  

Aún asi el tema de los PIDs es extenso y podemos ocasionar **daños** en el quad.  
Recomiendo mirar los diferentes videos antes de hacer cualquier cambio si no dominamos en este campo.   

Español:

[QuadMx - PIDs v4.2] https://www.youtube.com/watch?v=peKCvpUwgF0

[QuadMx - Propwash v4.0] https://www.youtube.com/watch?v=MHbk5iikqzw

[QuadMx - Filtros y PIDs v4.0] https://www.youtube.com/watch?v=QA1332j9dAM

Ingles:

[Joshua Bardwell - Presets Betaflight] https://www.youtube.com/watch?v=eFTnlhQRCFo

[Joshua Bardwell - PID en quad 6S] https://www.youtube.com/watch?v=m0uPllhGZts

[Manual PID Tuning Tutorial] https://www.youtube.com/watch?v=04Ixyomu9d8
