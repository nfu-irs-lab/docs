# 3D 列印機

## 目錄
- [Creality CR-5 Pro](#creality-cr-5-pro)
- [Creality Ender-5 Pro](#creality-ender-5-pro)

---

# Creality CR-5 Pro

## 列印範圍

- 列印平臺形狀：Rectangular （長方形）
- X：`300` mm
- Y：`225` mm
- Z：`380` mm

## 擠出機
- 數量：`1`
- 擠出頭孔直徑：`0.4` mm
- 相容的線材直徑：`1.75` mm

## 其它
- 原點位於中心：`false`
- 熱床：`true`
- G-Code類型：Marlin

## 機臺起始 G-Code
```gcode
; Creality CR-5 Pro Start G-Code.
M201 X500.00 Y500.00 Z100.00 E5000.00 ;Setup machine max acceleration
M203 X500.00 Y500.00 Z10.00 E50.00 ;Setup machine max feedrate
M204 P500.00 R1000.00 T500.00 ;Setup Print/Retract/Travel acceleration
M205 X8.00 Y8.00 Z0.40 E5.00 ;Setup Jerk
M220 S100 ;Reset Feedrate
M221 S100 ;Reset Flowrate

G28 ;Home

G92 E0 ;Reset Extruder
G1 Z2.0 F3000 ;Move Z Axis up
G1 X10.1 Y20 Z0.28 F5000.0 ;Move to start position
G1 X10.1 Y200.0 Z0.28 F1500.0 E15 ;Draw the first line
G1 X10.4 Y200.0 Z0.28 F5000.0 ;Move to side a little
G1 X10.4 Y20 Z0.28 F1500.0 E30 ;Draw the second line
G92 E0 ;Reset Extruder
G1 Z2.0 F3000 ;Move Z Axis up
;End of custom G-Code.
```

## 機臺結束 G-Code
```gcode
; Creality CR-5 Pro End G-Code.
G91 ;Relative positionning
G1 E-2 F2700 ;Retract a bit
G1 E-2 Z0.2 F2400 ;Retract and raise Z
G1 X5 Y5 F3000 ;Wipe out
G1 Z10 ;Raise Z more
G90 ;Absolute positionning

G1 X0 Y{machine_depth} ;Present print
M106 S0 ;Turn-off fan
M104 S0 ;Turn-off hotend
M140 S0 ;Turn-off bed

M84 X Y E ;Disable all steppers but Z
;End of custom G-Code.
```

# Creality Ender-5 Pro

## 列印範圍

- 列印平臺形狀：Rectangular （長方形）
- X：`220` mm
- Y：`220` mm
- Z：`300` mm

## 擠出機
- 數量：`1`
- 擠出頭孔直徑：`0.4` mm
- 相容的線材直徑：`1.75` mm

## 其它
- 原點位於中心：`false`
- 熱床：`true`
- G-Code類型：Marlin

## 機臺起始 G-Code
```gcode
; Creality Ender-5 Pro Start G-Code.
M201 X500.00 Y500.00 Z100.00 E5000.00 ;Setup machine max acceleration
M203 X500.00 Y500.00 Z10.00 E50.00 ;Setup machine max feedrate
M204 P500.00 R1000.00 T500.00 ;Setup Print/Retract/Travel acceleration
M205 X8.00 Y8.00 Z0.40 E5.00 ;Setup Jerk
M220 S100 ;Reset Feedrate
M221 S100 ;Reset Flowrate

G28 ;Home

G92 E0 ;Reset Extruder
G1 Z2.0 F3000 ;Move Z Axis up
G1 X10.1 Y20 Z0.28 F5000.0 ;Move to start position
G1 X10.1 Y200.0 Z0.28 F1500.0 E15 ;Draw the first line
G1 X10.4 Y200.0 Z0.28 F5000.0 ;Move to side a little
G1 X10.4 Y20 Z0.28 F1500.0 E30 ;Draw the second line
G92 E0 ;Reset Extruder
G1 Z2.0 F3000 ;Move Z Axis up
;End of custom G-Code.
```

## 機臺結束 G-Code
```gcode
; Creality Ender-5 Pro End G-Code.
G91 ;Relative positioning
G1 E-2 F2700 ;Retract a bit
G1 E-2 Z0.2 F2400 ;Retract and raise Z
G1 X5 Y5 F3000 ;Wipe out
G1 Z10 ;Raise Z more
G90 ;Absolute positioning

G1 X0 Y0 Present print
M106 S0 ;Turn-off fan
M104 S0 ;Turn-off hotend
M140 S0 ;Turn-off bed

M84 X Y E ;Disable all steppers but Z
;End of custom G-Code.
```
