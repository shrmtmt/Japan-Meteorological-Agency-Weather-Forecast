# 気象庁が過去に発表した天気予報のアーカイブ（履歴）  
日本の気象庁が過去に発表した天気予報のアーカイブです。過去の天気予報を調べる方法が公的には用意されていないため、個人的に日々の天気予報を定期的に取得していました。本データを用いれば、過去の天気予報の履歴を確認できます。

"forecast"と"overview forecast"の2種類のデータがあります。  
他に"overview_week"というのもあったのですが、更新・公開が止まってしまったようです。  
収集元は以下のURL形式、以下の期間です。  

- 予報(forecast)  
  - jsonファイルを月単位にまとめ地域毎のcsvファイルにし、全地域・1ヶ月分のcsvファイルをzip圧縮しています  
  - ソース: https://www.jma.go.jp/bosai/forecast/data/forecast/{region_code}.json  
  - 期間：2021-11-04 から2024-03-31まで
  - 収集間隔: 1日3回前後
    - 基本的には1日3回
    - 一部の日・地域に取得漏れあり
    - 定時発表に加え訂正報があった場合、１日４回以上になることもあり   
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
  - 期間：2021-12-15から2024-03-31まで  
  - 収集間隔 1日3回前後（同上）   
  - ファイル名:    
    - overview_forecast_yyyyMM_{地域コード}.csv  
  - 地域コード: '010000'を除き上記に同じ（'010000'は含まれない）

本サイトの天気予報や降水確率のデータを使用される場合、使用許諾等の事前の手続きは必要ありません。ご自由にご利用下さい。
論文や文章にデータの引用元を表示する際には、「CC BY-SA 4.0　原典：気象庁　アーカイブ：松本志朗」等と記載してください。
公開可能な研究などであれば、事後で構いませんので、「こんな形で利用しました」とお知らせいただけると大変うれしいです。
  
# Japan-Meteorological-Agency-Weather-Forecast
## Archive of past weather forecasts by the Japan Meteorological Agency  
This is an archive of past weather forecasts issued by the Japan Meteorological Agency. Since there is no publicly available way to check past weather forecasts, I personally obtained daily weather forecasts on a regular basis. With this data, you can check the history of past weather forecasts.

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
  - Period: from 2021-11-04 to 2024-02-29 (In some region: from 2021-12-15)  
  - Collection interval Around 3 times a day
    - There is a possibility of omission of acquisition
    - In case of correction reports in addition to regular announcements, it may be more than 4 times a day
  - File name:  
    - yyyyMM_{region_code}_ansi.csv  
    - yyyyMM_{region_code}_utf8.csv  
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
    - Region code: 010000 is the national forecast.  

- overview forecast
  - It contains information roughly similar to that found on the following pages.  
    [https://www.jma.go.jp/bosai/forecast/data/overview_forecast/130000.json](https://www.jma.go.jp/bosai/forecast/data/overview_forecast/130000.json)  
  - The orginal json files are grouped by month into csv files.  
  - Source: https://www.jma.go.jp/bosai/forecast/data/overview_forecast/{region_code}.json  
  - Period: from 2021-12-15 to 2021-09-30  
  - Collection interval: Around 3 times a day (same as above)   
  - File name:  
    - overview_forecast_yyyyMM_{Region code}.csv  
  - Region code: almost same as above, but '010000' is not included）

No prior permission is required to use the weather forecast and precipitation probability data on this site. Please feel free to use the data. 
When citing data in a paper or text, please state "CC BY-SA 4.0 Source: Japan Meteorological Agency Archive: Shiro Matsumoto" or the like. 
If your research can be made public, it would be greatly appreciated if you could inform me after that you published.
