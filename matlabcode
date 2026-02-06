% ------------------------------------------------------------
% Thermal Effects on Air Brake Efficiency in Railway Wagons
% ------------------------------------------------------------

clc;
clear;
close all;

%% -------------------- Constants --------------------
R = 287;            % Specific gas constant for air (J/kg·K)
k = 1.4;            % Adiabatic index for air
P = 8e5;            % Brake pipe pressure (Pa) = 8 bar
pipe_length = 350;  % Length of brake pipe (m)

%% -------------------- Temperature Range --------------------
T_C = [-10 0 25 40 50];   % Ambient temperature in Celsius
T_K = T_C + 273.15;      % Convert to Kelvin

%% -------------------- Initialize Arrays --------------------
air_density   = zeros(size(T_K));
sound_speed   = zeros(size(T_K));
response_time = zeros(size(T_K));

%% -------------------- Calculations --------------------
for i = 1:length(T_K)
    T = T_K(i);

    % Air density using Ideal Gas Law
    air_density(i) = P / (R * T);

    % Speed of pressure wave (sound speed)
    sound_speed(i) = sqrt(k * R * T);

    % Brake response time (pressure wave travel time)
    response_time(i) = pipe_length / sound_speed(i);
end

%% -------------------- Plot 1: Air Density vs Temperature --------------------
figure;
plot(T_C, air_density, '-o', 'LineWidth', 2);
xlabel('Ambient Temperature (°C)');
ylabel('Air Density (kg/m^3)');
title('Air Density vs Temperature');
grid on;

%% -------------------- Plot 2: Pressure Wave Speed vs Temperature --------------------
figure;
plot(T_C, sound_speed, '-s', 'LineWidth', 2);
xlabel('Ambient Temperature (°C)');
ylabel('Pressure Wave Speed (m/s)');
title('Pressure Wave Speed vs Temperature');
grid on;

%% -------------------- Plot 3: Brake Response Time vs Temperature --------------------
figure;
plot(T_C, response_time, '-d', 'LineWidth', 2);
xlabel('Ambient Temperature (°C)');
ylabel('Brake Response Time (s)');
title('Brake Response Time vs Temperature');
grid on;

%% -------------------- Display Results --------------------
disp('Temperature (°C) | Air Density (kg/m^3) | Wave Speed (m/s) | Response Time (s)');
disp([T_C' air_density' sound_speed' response_time']);
