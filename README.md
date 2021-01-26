tessdata

(1) 下載tess4j-4.5.4.jar

    tess4j是hp 在20sh世紀90年代研發，最後貢獻給google 的 開源專案 自版本3.0.2後支援了對中文字型檔的識別
    <dependency>
      <groupId>net.sourceforge.tess4j</groupId>
      <artifactId>tess4j</artifactId>
      <version>4.5.4</version>
    </dependency>

(2) 下載語言包 tessdata (https://github.com/YenCheChangGoogle/tessdata) 資料解壓縮後 放置於 D:/Senao/github.com/SpringBoot2RestAPI/utils/OCR/tessdata-master 目錄

(3) 識別中文所以下載語言包 chi 字眼開頭的 chi_sim.traineddata, chi_sim_vert.traineddata, chi_tra.traineddata, chi_tra_vert.traineddata, chr.traineddata

(4) jdk 版本必須1.7以上

========

These language data files only work with Tesseract 4.0.0 and newer versions.
They are based on the sources in
[tesseract-ocr/langdata](https://github.com/tesseract-ocr/langdata) on GitHub.
(still to be updated for 4.0.0 - 20180322)

These have models for legacy tesseract engine (--oem 0) as well as the new LSTM neural net based engine (--oem 1).

The LSTM models (--oem 1) in these files 
have been updated to the integerized versions of 
[tessdata_best](https://github.com/tesseract-ocr/tessdata_best) on GitHub.
So, they should be faster but probably a little less accurate than tessdata_best.

[tessdata_fast](https://github.com/tesseract-ocr/tessdata_fast) on GitHub
provides an alternate set of integerized LSTM models which have been built with a smaller network.
tessdata_fast files are the ones packaged for Debian and Ubuntu.

The legacy tesseract models (--oem 0) have been removed for Indic and
Arabic script language files.

tessdata for 3.04 or 3.05
-------------------------

Get language data files for Tesseract 3.04 or 3.05 from the
[3.04 tree](https://github.com/tesseract-ocr/tessdata/tree/3.04.00).

More information and a complete list of all languages is available in the
[Tesseract wiki](https://github.com/tesseract-ocr/tesseract/wiki/Data-Files).

All data in the repository are licensed under the
Apache-2.0 License, see file [LICENSE](LICENSE).
