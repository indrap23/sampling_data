# Tugas 4 SQL & Sheel Toolings
## Username : indra-qcl9
### Penjelasan code tugas 4
1. Download data menggunakan wget
```bash
wget -P ./data https://github.com/labusiam/dataset/raw/main/weather_data.xlsx
```
2. convert each sheet to csv. and save to folder data with name's weather_2014.csv and weather_2015.csv
```bash
in2csv ./data/weather_data.xlsx --sheet "weather_2014" > ./data/weather_2014.csv
in2csv ./data/weather_data.xlsx --sheet "weather_2015" > ./data/weather_2015.csv
```
3. append weather_2014.csv and weather_2015.csv and save to folder data with name's weather.csv
```bash
csvstack ./data/weather_2014.csv ./data/weather_2015.csv > ./data/weather.csv
```
4. sampling data weather.csv with sample rate 0.3 and save to folder data with name's sample_weather.csv
```bash
cat ./data/weather.csv | sample -r 0.3 > ./data/sample_weather.csv
```