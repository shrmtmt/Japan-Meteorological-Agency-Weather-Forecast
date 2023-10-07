# Japan-Meteorological-Agency-Weather-Forecast
## Archive of past weather forecasts by the Japan Meteorological Agency  
The collection sources are the following URL formats and the following time periods.  
I will refrain from explaining how to read each data item, as the JMA does not have officially announced it.  
I ask that you make your own guesses by checking the JMA's web page.  
There are two types of data: "forecast" and "overview_forecast".
There was another "overview_week" but it seems to have stopped being updated, so it has not been published.

- forecast
  - It contains information roughly similar to that found on the following pages.  
    [https://www.jma.go.jp/bosai/forecast/data/forecast/130000.json](https://www.jma.go.jp/bosai/forecast/data/forecast/130000.json)  
  - The orginal json files are grouped by month into csv files.  
  - Source: https://www.jma.go.jp/bosai/forecast/data/forecast/{region_code}.json  
  - Period: from 2021-11-04 or 2021-12-15 (depend on region) to 2023-09-30  
  - Collection interval 3 times a day (possible omissions, corrections may be made in addition to regular announcements)   
  - File name:  
    - yyyyMM_{region_code}_ansi.csv  
    - yyyyMM_{region_code}_utf8.csv  
  - Region code: [  
                '011000', '012000', '013000', '014100', '015000', '016000', '017000', '020000',   
                '030000', '040000', '050000', '060000', '070000', '080000', '090000', '100000',  
                '110000', '120000', '130000', '140000', '150000', '160000', '170000', '180000',  
                '190000', '200000', '210000', '220000', '230000', '240000', '250000', '260000',  
                '270000', '280000', '290000', '300000', '310000', '320000', '330000', '340000',  
                '350000', '360000', '370000', '380000', '390000', '400000', '410000', '420000',  
                '430000', '440000', '450000', '460100', '471000', '472000', '473000', '474000'  
                ]  
    - Region code: 010000 is omitted because of informational redundancy in the national forecast.  

- overview forecast
  - It contains information roughly similar to that found on the following pages.  
    [https://www.jma.go.jp/bosai/forecast/data/overview_forecast/130000.json](https://www.jma.go.jp/bosai/forecast/data/overview_forecast/130000.json)  
  - The orginal json files are grouped by month into csv files.  
  - Source: https://www.jma.go.jp/bosai/forecast/data/overview_forecast/{region_code}.json  
  - Period: from 2021-12-15 to 2021-09-30  
  - Collection interval: 3 times a day (there may be omissions, corrections may be made in addition to regular announcements)   
  - File name:  
    - yyyyMM_{region_code}_ansi.csv  
    - yyyyMM_{region_code}_utf8.csv  
  - Region code: same as above  

# 日本の気象庁による過去の天気予報のアーカイブ  
収集元は以下のURL形式、以下の期間です。  
各データ項目の読み取り方は、気象庁が公式に発表していないこともあり、私からは説明を控えます。
気象庁のwebページの記載と照らし合わせて各自推測していただけますようお願いします。
"forecast"と"overview forecast"の2種類のデータがあります。
他に"overview_week"というのもあったのですが、更新が止まってしまったようなので公開していません。

- 予報(forecast)  
  - jsonファイルを月単位にまとめcsvファイルにしています  
  - ソース: https://www.jma.go.jp/bosai/forecast/data/forecast/{region_code}.json  
  - 期間：2021-11-04 または 2021-12-15 (地域コードにより異なる) から2023-09-30まで  
  - 収集間隔: 1日3回（漏れがある可能性あり、定時発表に加え訂正がなされることもあり）   
  - ファイル名:    
    - yyyyMM_{地域コード}_ansi.csv  
    - yyyyMM_{地域コード}_utf8.csv  
  - 地域コード: 上記に同じ  
    - 地域コード 010000 は全国予報であり、情報的には上記に包含されるため略しています
   
- 概要予報(overview forecast)  
  - jsonファイルを月単位にまとめcsvファイルにしています  
  - ソース https://www.jma.go.jp/bosai/forecast/data/overview_forecast/{region_code}.json  
  - 期間：2021-12-15から2021-09-30まで  
  - 収集間隔 1日3回（漏れがある可能性あり）   
  - ファイル名:  
    - yyyyMM_{地域コード}_ansi.csv  
    - yyyyMM_{地域コード}_utf8.csv  
  - 地域コード: 上記に同じ
  
