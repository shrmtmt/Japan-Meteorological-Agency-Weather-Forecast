# 気象庁が過去に発表した天気予報のアーカイブ（履歴データベース）  
日本の気象庁が過去に発表した天気予報のアーカイブ（履歴データベース）です。過去の実際の天気はさかのぼって入手することができますが、過去の天気**予報**は公的に提供されていないため、個人的に日々の天気予報を定期的に取得していました。本データを用いれば、過去の天気予報の履歴を確認できます。

詳細天気予報"forecast"と概要予報"overview forecast"の2種類のデータがあります。  
他に全般週間天気予報"overview_week"というのもあったのですが、更新・公開が止まってしまったようです。  
収集元は以下のURL形式、以下の期間です。  

- 予報(forecast)  
  - jsonファイルを月単位にまとめ地域毎のcsvファイルにし、全地域・1ヶ月分のcsvファイルをzip圧縮しています  
  - ソース: https://www.jma.go.jp/bosai/forecast/data/forecast/{region_code}.json  
  - 期間：2021-11-04 以降
  - 収集間隔: 1日3回前後
    - 基本的には1日3回
    - 一部の日・地域に取得漏れあり
    - 定時発表に加え訂正報があった場合、1日4回以上になることもあり   
  - ファイル名:    
    - forecast_yyyyMM_{地域コード}.csv  
  - 地域コード: [  
                '010000',
                '011000', '012000', '013000', '014100', '015000', '016000', '017000', '020000',   
                '030000', '040000', '050000', '060000', '070000', '080000', '090000', '100000',  
                '110000', '120000', '130000', '140000', '150000', '160000', '170000', '180000',  
                '190000', '200000', '210000', '220000', '230000', '240000', '250000', '260000',  
                '270000', '280000', '290000', '300000', '310000', '320000', '330000', '340000',  
                '350000', '360000', '370000', '380000', '390000', '400000', '410000', '420000',  
                '430000', '440000', '450000', '460100', '471000', '472000', '473000', '474000'  
                ]  
    - 地域コード 010000 は全国予報です
   
- 概要予報(overview forecast)  
  - jsonファイルを月単位にまとめ地域毎のcsvファイルにし、全地域・1ヶ月分のcsvファイルをzip圧縮しています  
  - ソース: https://www.jma.go.jp/bosai/forecast/data/overview_forecast/{region_code}.json  
  - 期間：2021-12-15 以降
  - 収集間隔 1日3回前後（同上）   
  - ファイル名:    
    - overview_forecast_yyyyMM_{地域コード}.csv  
  - 地域コード: '010000'を除き上記に同じ（'010000'は含まれない）

本サイトの天気予報や降水確率のデータを使用される場合、使用許諾等の事前の手続きは必要ありません。ご自由にご利用下さい。
公開可能な研究などであれば、事後で構いませんので、「こんな形で利用しました」とIssueのコメントなどでお知らせいただけるとモチベがあがります。

# Japan-Meteorological-Agency-Weather-Forecast
## Archive of past weather forecasts by the Japan Meteorological Agency  
This is an archive of past weather forecasts the Japan Meteorological Agency issued. Since there is no publicly available way to check past weather forecasts, I obtained daily weather forecasts regularly. With this data, you can check the history of past weather forecasts.

The collection sources are the following URL formats and the following periods.  
There are two types of data: "forecast" and "overview_forecast."
There was another "overview_week," but it seems to have stopped being updated, so it has not been published.

- forecast
  - It contains information roughly similar to that found on the following pages.
    [https://www.jma.go.jp/bosai/forecast/data/forecast/130000.json](https://www.jma.go.jp/bosai/forecast/data/forecast/130000.json)
  - The original JSON files are grouped by month into CSV files.
  - Source: https://www.jma.go.jp/bosai/forecast/data/forecast/{region_code}.json
  - Period: from 2021-11-04
  - Collection interval: Around 3 times a day
    - There is a possibility of omission of acquisition
    - In case of correction reports in addition to regular announcements, it may be more than 4 times a day
  - File name:
    - yyyyMM_{region_code}.csv
  - Region code: [  
                '010000',
                '011000', '012000', '013000', '014100', '015000', '016000', '017000', '020000',   
                '030000', '040000', '050000', '060000', '070000', '080000', '090000', '100000',  
                '110000', '120000', '130000', '140000', '150000', '160000', '170000', '180000',  
                '190000', '200000', '210000', '220000', '230000', '240000', '250000', '260000',  
                '270000', '280000', '290000', '300000', '310000', '320000', '330000', '340000',  
                '350000', '360000', '370000', '380000', '390000', '400000', '410000', '420000',  
                '430000', '440000', '450000', '460100', '471000', '472000', '473000', '474000'  
                ]  
    - Region code 010000 is the national forecast.  

- overview forecast
  - It contains information roughly similar to that found on the following pages.  
    [https://www.jma.go.jp/bosai/forecast/data/overview_forecast/130000.json](https://www.jma.go.jp/bosai/forecast/data/overview_forecast/130000.json)  
  - The original JSON files are grouped by month into CSV files.  
  - Source: https://www.jma.go.jp/bosai/forecast/data/overview_forecast/{region_code}.json  
  - Period: from 2021-12-15  
  - Collection interval: Around 3 times a day (same as above)   
  - File name:  
    - overview_forecast_yyyyMM_{Region code}.csv  
  - Region code: almost same as above, but '010000' is not included）

You don't need any prior permission to use the weather forecast and precipitation probability data on this site. Please feel free to use the data. 
If your research can be made public, I would greatly appreciate it if you could inform me via issue comments after you publish.
