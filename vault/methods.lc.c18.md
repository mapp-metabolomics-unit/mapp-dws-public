---
id: 3zx39e8tdcthecaokha495h
title: C18
desc: ''
updated: 1726638427413
created: 1726638352644
---



---- Overview ----
Name: New Instrument Method
Comment: 
Run time: 15.000 [min]
Instrument: Vanquish on qexactiveplus
Description: 
---- Script ----
initial     Instrument Setup
            ColumnComp.PrehtLeft.ReadyTempDelta: 1.00 [°C]
            ColumnComp.PrehtLeft.TempCtrl: On
            ColumnComp.PrehtLeft.Temperature.Nominal: 40.00 [°C]
            ColumnComp.PrehtLeft.EquilibrationTime: 1.0 [min]
            ColumnComp.CC.Mode: StillAir
            ColumnComp.CC.ReadyTempDelta: 1.00 [°C]
            ColumnComp.CC.TempCtrl: On
            ColumnComp.CC.Temperature.Nominal: 40.00 [°C]
            ColumnComp.CC.EquilibrationTime: 1.0 [min]
            ColumnComp.Column_A.SystemPressure: "Pump"
            ColumnComp.Column_B.ActiveColumn: No
            ColumnComp.Column_B.SystemPressure: "Pump"
            ColumnComp.Column_C.ActiveColumn: No
            ColumnComp.Column_C.SystemPressure: "Pump"
            ColumnComp.Column_D.ActiveColumn: No
            ColumnComp.Column_D.SystemPressure: "Pump"
            SamplerModule.Sampler.PunctureOffset: 0 [µm]
            SamplerModule.Sampler.WashSpeed: 10.0 [µl/s]
            SamplerModule.Sampler.InjectWashMode: Both
            SamplerModule.Sampler.WashTime: 2.0 [s]
            SamplerModule.Sampler.DispenseSpeed: 5.000 [µl/s]
            SamplerModule.Sampler.DrawSpeed: 5.000 [µl/s]
            SamplerModule.Sampler.Pump: "Pump"
            SamplerModule.TempCtrl: On
            SamplerModule.Temperature.Nominal: 10.0 [°C]
            PumpModule.Pump.%B_Selector: %B1
            PumpModule.Pump.%A_Selector: %A1
            PumpModule.Pump.%A1_Equate: "H2O"
            PumpModule.Pump.%A2_Equate: "%A2"
            PumpModule.Pump.%A3_Equate: "%A3"
            PumpModule.Pump.%B1_Equate: "ACN"
            PumpModule.Pump.%B2_Equate: "%B2"
            PumpModule.Pump.%B3_Equate: "%B3"
            PumpModule.Pump.Pressure.LowerLimit: 0 [bar]
            PumpModule.Pump.Pressure.UpperLimit: 1000 [bar]
            PumpModule.Pump.MaximumFlowRampUp: 6.00 [ml/min²]
            PumpModule.Pump.MaximumFlowRampDown: 6.00 [ml/min²]
0.000 [min] Inject Preparation
            Wait ColumnComp.Ready And SamplerModule.Sampler.Ready And PumpModule.Pump.Ready
0.000 [min] Inject
            SamplerModule.Sampler.Inject 
0.000 [min] Start Run
            ColumnComp.CC_Temp.AcqOn 
            ColumnComp.PrehtLeft_Temp.AcqOn 
            PumpModule.Pump.Pump_Pressure.AcqOn 
0.000 [min] Run
            PumpModule.Pump.Flow.Nominal: 0.600 [ml/min]
            PumpModule.Pump.%B.Value: 2.0 [%]
            PumpModule.Pump.Curve: 5
10.000 [min]
            PumpModule.Pump.Flow.Nominal: 0.600 [ml/min]
            PumpModule.Pump.%B.Value: 100.0 [%]
            PumpModule.Pump.Curve: 5
12.000 [min]
            PumpModule.Pump.Flow.Nominal: 0.600 [ml/min]
            PumpModule.Pump.%B.Value: 100.0 [%]
            PumpModule.Pump.Curve: 5
12.200 [min]
            PumpModule.Pump.Flow.Nominal: 0.600 [ml/min]
            PumpModule.Pump.%B.Value: 2.0 [%]
            PumpModule.Pump.Curve: 5
15.000 [min]
            PumpModule.Pump.Flow.Nominal: 0.600 [ml/min]
            PumpModule.Pump.%B.Value: 2.0 [%]
            PumpModule.Pump.Curve: 5
15.000 [min] Stop Run
            ColumnComp.CC_Temp.AcqOff 
            ColumnComp.PrehtLeft_Temp.AcqOff 
            PumpModule.Pump.Pump_Pressure.AcqOff 


