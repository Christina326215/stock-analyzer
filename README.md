# stock-analyzer

* 本專案針對3大產業類別進行分析，財務股價資訊來自台灣證券交易所，個股日成交資訊/個股日本益比、殖利率、股價淨值比。

* 以下是資料來源取得步驟，抓取資料時為加快速度採平行處理(threading):
    1. 安裝 Selenium 工具
    2. 利用 Selenium & Beautiful Soup 抓取民國99年至民國112年各月份個股日成交資訊/個股日本益比、殖利率、股價淨值比
    3. 儲存成 csv

* 三大產業類別資料之股票如下:
    1. AI產業: '2454','2330','6214','2308','2357','2353'
    2. 電腦業: '2377', '2324', '2356', '2376', '3231', '8215'
    3. 紡織業: '1414', '1434', '1451', '1457', '1476', '1477'

* 資料自csv取得，開始進行資料處理，採numpy、pandas:
    1. 處理異常資料值及資料格式轉換
    2. 個股取資料年月之交集(個股皆有的資料月份才納入後續計算)
    3. 分成x_values、y_values，開始進行資料(預測分群)分析

* 如下是資料分析方法，並以Matplotlib呈現:
1. PCA & KMeans
2. TSNE
3. SVD
