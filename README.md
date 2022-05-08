# sampling_data

### Penjelasan isi dari sampling.sh

```
wget -O weather_data.xlsx https://github.com/labusiam/dataset/raw/main/weather_data.xlsx
```
download file excel dari link dan menyimpannya dengan nama weather_data.xlsx

```
in2csv weather_data.xlsx --sheet "weather_2014" > weather_2014.csv
```
mengkonvert sheet weather_2014 pada weather_data.xlsx ke weather_2014.csv

```
in2csv weather_data.xlsx --sheet "weather_2015" > weather_2015.csv
```
mengkonvert sheet weather_2014 pada weather_data.xlsx ke weather_2014.csv

```
csvstack weather_2014.csv weather_2015.csv >> weather.csv
```
menggabungkan weather_2014.csv dan weather_2015.csv ke dalam file weather.csv

```
rm weather_data.xlsx
```
menghapus file weather_data.xlsx

```
csvlook weather.csv | sample -r 30% >> sample_weather.csv
```
sampling data dalam file weather.csv dengan rate 0.3 lalu menyimpannya ke dalam file sample_weather.csv
