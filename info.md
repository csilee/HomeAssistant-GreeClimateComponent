# Egyedi Gree klímaintegráció. Vezérli a Gree protokollt támogató AC-kat.

## Komponens konfiguráció

Az összetevő konfigurálásához adja hozzá a következő konfigurációt a configuration.yaml fájlhoz (a helyőrzők helyére).

```
 climate:
   - platform: gree
     name: Első AC
     host: <az első AC ip címe>
     port: 7000
     mac: '<az első AC mac címe>'
     target_temp_step: 1
     encryption_key: <OPCIONÁLIS: egyéni titkosítási kulcs, ha a wifi már konfigurálva van>
     uid: <valamilyen eszközazonosító. MEGJEGYZÉS: egyes készülékeknél ez opcionális>
     temp_sensor: <a hőmérséklet-érzékelő entitásazonosítója. Például: sensor.nappali_temperature>
     lights: <OPCIONÁLIS: input_boolean az AC kijelzővilágítás be- és kikapcsolásához. Például:input_boolean.elso_ac_lights>
     xfan: <OPCIONÁLIS: input_boolean to switch AC xfan mode on/off. For example: input_boolean.first_ac_xfan>
     health: <OPCIONÁLIS: input_boolean used to switch the Health option on/off of your first AC. For example: input_boolean.first_ac_health>
     sleep: <OPCIONÁLIS: input_boolean to switch AC sleep mode on/off. For example: input_boolean.first_ac_sleep>
     powersave: <OPCIONÁLIS: input_boolean to switch AC powersave mode on/off. For example: input_boolean.first_ac_powersave>
   
   - platform: gree
     name: Második AC
     host: <a második AC ip címe>
     port: 7000
     mac: '<a második AC mac címe>'
     target_temp_step: 1
```
