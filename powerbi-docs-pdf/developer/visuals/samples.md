---
title: ตัวอย่างวิชวล Power BI ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: บทความนี้แสดงตัวอย่างวิชวล Power BI ประกอบไปด้วยแบ่งส่วนข้อมูล แผนภูมิมากกว่า20ชนิด WebGL รวมถึง วิชวล R และสคริปต์ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: sranins
ms.service: powerbi
ms.subservice: powerbi-custom-visuals
ms.topic: reference
ms.date: 03/17/2019
ms.openlocfilehash: 3da805a10a8b43dc7b1f1750583a79494557d519
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97888500"
---
# <a name="samples-of-power-bi-visuals"></a>ตัวอย่างสำหรับวิชวล Power BI

คุณสามารถดาวน์โหลด ใช้ และปรับเปลี่ยนวิชวล Power BI เหล่านี้ได้จาก GitHub ตัวอย่างเหล่านี้แสดงวิธีการจัดการสถานการณ์ทั่วไปเมื่อพัฒนาด้วย Power BI

## <a name="slicers"></a>ตัวแบ่งส่วนข้อมูล

ตัวแบ่งส่วนข้อมูลจะจำกัดส่วนของข้อมูลที่แสดงอยู่ในการแสดงภาพอื่นๆ ในรายงาน ตัวแบ่งส่วนข้อมูลเป็นหนึ่งในหลายวิธีในการกรองข้อมูลใน Power BI

| <img src="media/samples/chiclet-slicer.png" alt="Screenshot shows Chiclet Slicer." width="200">  | <img src="media/samples/timeline-slicer.png" alt="Screenshot shows Timeline slicer." width="200"> | <img src="media/samples/sample-slicer.png" alt="Screenshot shows Slicer sample." width="200">|
| ------------- | ------------- | -------------|
| [Chiclet Slicer](https://github.com/Microsoft/powerbi-visuals-chicletslicer/)  </br>แสดงรูปภาพหรือปุ่มข้อความที่ทำหน้าที่เป็นตัวกรองกราฟิกในพื้นที่บนวิชวลอื่น ๆ | [Timeline Slicer](https://github.com/Microsoft/powerbi-visuals-timeline/) </br>ตัวเลือกช่วงวันที่แบบกราฟิกที่กรองตามวันที่ | [ตัวอย่างตัวแบ่งส่วนข้อมูล](https://github.com/Microsoft/powerbi-visuals-sampleslicer/) </br>อธิบายการใช้ API การกรองขั้นสูง

## <a name="charts"></a>แผนภูมิ

รับแรงบันดาลใจจากแกลเลอรีของเรา ที่ประกอบด้วยแผนภูมิแท่ง แผนภูมิวงกลม  Word Cloud และอื่นๆ

| <img src="media/samples/aster-plot.png" alt="Screenshot shows Aster Plot." width="200">  | <img src="media/samples/bullet-chart.png" alt="Screenshot shows Bullet chart." width="200"> | <img src="media/samples/Chord.png" alt="Screenshot shows Chord." width="200">|
| ------------- | ------------- | -------------|
| [Aster Plot](https://github.com/Microsoft/powerbi-visuals-asterplot/)  </br>แนวทางใหม่สำหรับแผนภูมิโดนัทมาตรฐาน ที่ใช้ค่าที่สองเพื่อลบมุม | [แผนภูมิหัวข้อย่อย](https://github.com/Microsoft/powerbi-visuals-bulletchart/) </br>แผนภูมิแท่งซึ่งมีองค์ประกอบภาพพิเศษที่ให้บริบท อันเป็นประโยชน์สำหรับการติดตามเป้าหมาย | [Chord](https://github.com/Microsoft/powerbi-visuals-chord/) </br>วิธีการทางกราฟิกที่แสดงความสัมพันธ์ของข้อมูลในเมทริกซ์
| <img src="media/samples/dot-plot.png" alt="Screenshot shows Dot plot." width="200"> | <img src="media/samples/dual-kpi.png" alt="Screenshot shows Dual K P I." width="200">| <img src="media/samples/enhanced-scatter.png" alt="Screenshot shows Enhanced Scatter." width="200"> 
| [การพล็อตด้วยจุด](https://github.com/Microsoft/powerbi-visuals-dotplot/) </br>แสดงการกระจายของความถี่ในรูปแบบที่ดูดี | [Dual KPI](https://github.com/Microsoft/powerbi-visuals-dualkpi/) </br>แสดงภาพหน่วยวัดสองรายการในช่วงเวลา แสดงแนวโน้มของรายการดังกล่าวบนเส้นเวลาร่วมกันได้อย่างมีประสิทธิภาพ | [Enhanced Scatter](https://github.com/Microsoft/powerbi-visuals-enhancedscatter/) </br>การปรับปรุงของแผนภูมิกระจายที่มีอยู่
| <img src="media/samples/forcegraph.png" alt="Screenshot shows Force Graph." width="200">| <img src="media/samples/gantt.png" alt="Screenshot shows Gantt." width="200">| <img src="media/samples/table-heatmap.png" alt="Screenshot shows Table Heatmap." width="200">
| [Force Graph](https://github.com/Microsoft/powerbi-visuals-forcegraph/) </br>บังคับเค้าโครงไดอะแกรมด้วยเส้นโค้ง ซึ่งประโยชน์ในการแสดงการเชื่อมต่อระหว่างเอนทิตี | [Gantt](https://github.com/Microsoft/powerbi-visuals-gantt/) </br>แผนภูมิแท่งที่แสดงเส้นเวลาโครงการหรือกำหนดการพร้อมทรัพยากร | [Table Heatmap](https://github.com/Microsoft/powerbi-visuals-heatmap/) </br>เปรียบเทียบข้อมูลได้อย่างง่ายดายและคล่องตัวโดยใช้สีในตาราง
| <img src="media/samples/histogram-chart.png" alt="Screenshot shows Histogram chart." width="200"> | <img src="media/samples/linedot-chart.png" alt="Screenshot shows LineDot chart." width="200"> | <img src="media/samples/mekko-chart.png" alt="Screenshot shows Mekko chart." width="200"> 
| [Histogram chart](https://github.com/Microsoft/powerbi-visuals-histogram/) </br>แสดงภาพการกระจายข้อมูลในช่วงเวลาต่อเนื่องหรือบางช่วงเวลา | [LineDot chart](https://github.com/Microsoft/powerbi-visuals-linedotchart/) </br>แผนภูมิเส้นแบบเคลื่อนไหวที่มีจุดเคลื่อนไหว ซึ่งจะดึงดูดให้ผู้ชมสนใจข้อมูล | [Mekko chart](https://github.com/Microsoft/powerbi-visuals-mekkochart/) </br>การผสมผสานของแผนภูมิคอลัมน์แบบเรียงซ้อน 100% และแผนภูมิแท่งแบบเรียงซ้อน 100% รวมอยู่ในมุมมองเดียว
| <img src="media/samples/multikpi.png"alt="Screenshot shows Multi K P I." width="200"> | <img src="media/samples/powerkpi.png"alt="Screenshot shows Power K P I." width="200"> | <img src="media/samples/powerkpi-matrix.png"alt="Screenshot shows Power K P I Matrix." width="200"> 
| [หลาย KPI](https://github.com/microsoft/PowerBI-visuals-MultiKPI/) </br> การแสดงภาพหลาย KPI อันทรงพลังด้วย KPI หลักพร้อมกับกราฟ Sparklines ที่มีข้อมูลที่สนับสนุนหลายรายการ | [Power KPI](https://github.com/microsoft/PowerBI-visuals-PowerKPI/) </br>ตัวบ่งชี้ KPI อันทรงพลัง ด้วยแผนภูมิหลายเส้นและป้ายชื่อสำหรับวันที่  มูลค่า และความแปรปรวนปัจจุบัน | [Power KPI Matrix](https://github.com/microsoft/PowerBI-visuals-PowerKPIMatrix/) </br>ตรวจสอบดัชนีชี้วัดที่สมดุลและจำนวนเมตริกและ KPI ที่ไม่ จำกัด ในรายการขนาดกะทัดรัดและอ่านง่าย
| <img src="media/samples/pulse-chart.png" alt="Screenshot shows Pulse chart." width="200">| <img src="media/samples/radar-chart.png" alt="Screenshot shows Radar chart." width="200"> | <img src="media/samples/sankey-chart.png" alt="Screenshot shows Sankey chart." width="200"> 
| [Pulse chart](https://github.com/Microsoft/powerbi-visuals-pulsechart/) </br>แผนภูมิเส้นนี้มีซึ่งมีคำอธิบายประกอบของเหตุการณ์สำคัญ เหมาะสำหรับการบอกเล่าเรื่องราวด้วยข้อมูล| [Radar chart](https://github.com/Microsoft/powerbi-visuals-radarchart/) </br>นำเสนอหลายหน่วยวัดที่ลงจุดบนแกนบอกประเภท ซึ่งมีประโยชน์ในการเปรียบเทียบคุณลักษณะ | [Sankey Chart](https://github.com/Microsoft/powerbi-visuals-sankey/) </br>แผนภาพกระแสข้อมูลที่ความกว้างของชุดข้อมูลเป็นสัดส่วนกับปริมาณของกระแสข้อมูล
| <img src="media/samples/stream-graph.png" alt="Screenshot shows Stream graph." width="200"> | <img src="media/samples/sunburst.png" alt="Screenshot shows Sunburst chart." width="200">| <img src="media/samples/tornado.png" alt="Screenshot shows Tornado chart." width="200">
| [Stream graph](https://github.com/Microsoft/powerbi-visuals-streamgraph/) </br>แผนภูมิพื้นที่แบบเรียงซ้อนที่มีการประมาณค่าในช่วงอย่างราบรื่น ซึ่งมักจะใช้ในการแสดงค่าในช่วงเวลาหนึ่ง | [Sunburst chart](https://github.com/Microsoft/powerbi-visuals-sunburst/) </br>แผนภูมิโดนัทหลายระดับสำหรับการแสดงภาพข้อมูลตามลำดับชั้น| [Tornado chart](https://github.com/Microsoft/powerbi-visuals-tornado/) </br>เปรียบเทียบความสำคัญเชิงสัมพัทธ์ของตัวแปรระหว่างสองกลุ่ม
 | <img src="media/samples/word-cloud.png" alt="Screenshot shows Word Cloud." width="200">
 | [Word Cloud](https://github.com/Microsoft/powerbi-visuals-wordcloud/) </br>สร้างวิชวลสนุกสนานจากข้อความในข้อมูลของคุณที่ใช้บ่อย

## <a name="webgl"></a>WebGL

WebGL อนุญาตให้เนื้อหาเว็บใช้ API ที่ยึดตาม OpenGL ES 2.0 เพื่อทำการแสดงภาพแบบ 2 มิติ และ 3 มิติ ในพื้นที่ทำงาน HTML

| <img src="media/samples/globe-map.png" alt="Screenshot shows Globe Map." width="250">|
| ------------- |
| [Globe Map](https://github.com/Microsoft/powerbi-visuals-globemap/) </br>ลงจุดตำแหน่งที่ตั้งลงบนแผนที่ 3 มิติแบบโต้ตอบ

## <a name="r-visuals"></a>วิชวล R

ตัวอย่างเหล่านี้สาธิตวิธีการใช้งานการวิเคราะห์และการแสดงผลด้วยภาพของวิชวล R และสคริปต์ R

| <img src="media/samples/association-rules.png" alt="Screenshot shows Association rules." width="200">| <img src="media/samples/clustering.png" alt="Screenshot shows Clustering." width="200">| <img src="media/samples/clustering-with-outliers.png" alt="Screenshot shows Clustering with outliers." width="200">|
|------------- |------------- |------------- |------------- |
| [กฎความสัมพันธ์](https://github.com/Microsoft/powerbi-visuals-assorules/) </br>แสดงความสัมพันธ์ระหว่างข้อมูลที่ดูไม่เกี่ยวข้องกันโดยการใช้คำสั่ง if-then | [การทำคลัสเตอร์](https://github.com/Microsoft/powerbi-visuals-clustering-kmeans/) </br>ค้นหากลุ่มที่คล้ายคลึงกันในข้อมูลของคุณโดยใช้อัลกอริทึม k-means | [การทำคลัสเตอร์กับค่าผิดปกติ](https://github.com/microsoft/PowerBI-visuals-dbscan/) </br>ค้นหากลุ่มที่คล้ายคลึงกันและค่าผิดปกติในข้อมูลของคุณ
| <img src="media/samples/correlation-plot.png" alt="Screenshot shows Correlation plot." width="200"> | <img src="media/samples/decision-tree-chart.png" alt="Screenshot shows Decision tree chart." width="200"> | <img src="media/samples/forecasting-tbats.png" alt="Screenshot shows Forecasting T B A T S." width="200"> 
| [การลงจุดค่าสหสัมพันธ์](https://github.com/Microsoft/powerbi-visuals-corrplot/) </br>เน้นตัวแปรที่สัมพันธ์กันมากที่สุดในตารางข้อมูล | [แผนผังต้นไม้การตัดสินใจ](https://github.com/Microsoft/powerbi-visuals-decision-tree/) </br>แผนผังรูปต้นไม้ที่เป็นแบบแผนสำหรับกำหนดความน่าจะเป็นทางสถิติโดยใช้การแบ่งพาร์ติชันแบบเรียกซ้ำ | [การคาดการณ์ TBATS](https://github.com/Microsoft/powerbi-visuals-forcasting-tbats/) </br>การพยากรณ์ชุดข้อมูลเวลาสำหรับชุดข้อมูลที่มีหลาย seasonality โดยใช้แบบจำลอง TBATS
| <img src="media/samples/forecasting-with-ARIMA.png" alt="Screenshot shows Forecasting with ARIMA." width="200"> | <img src="media/samples/funnel-plot.png" alt="Screenshot shows Funnel plot." width="200"> | <img src="media/samples/outliers-detection.png" alt="Screenshot shows Outliers detection." width="200"> 
| [การคาดการณ์ด้วย ARIMA](https://github.com/Microsoft/powerbi-visuals-forcastingarima/) </br>ทำนายค่าในอนาคตโดยยึดตามข้อมูลในอดีตโดยใช้ Autoregressive Integrated Moving Avg (ARIMA) | [กราฟกรวยคว่ำ](https://github.com/Microsoft/powerbi-visuals-funnel/) </br>ค้นหาค่าผิดปกติในข้อมูลของคุณโดยใช้กราฟกรวยคว่ำ | [การตรวจจับค่าผิดปกติ](https://github.com/Microsoft/powerbi-visuals-outliers-det/) </br>ค้นหาค่าผิดปกติในข้อมูลของคุณโดยใช้วิธีการและการพล็อตกราฟที่เหมาะสมที่สุด
| <img src="media/samples/spline-chart.png" alt="Screenshot shows Spline chart." width="200"> | <img src="media/samples/time-series-decomposition-chart.png" alt="Screenshot shows Time Series decomposition chart." width="200"> | <img src="media/samples/time-series-forecasting-chart.png" alt="Screenshot shows Time series forecasting chart." width="200">
| [Spline chart](https://github.com/Microsoft/powerbi-visuals-spline/) </br>แสดงภาพและทำความเข้าใจข้อมูลรบกวน | [แผนภูมิ Time series decomposition](https://github.com/Microsoft/powerbi-visuals-timeseriesdecomposition/) </br>ทำความเข้าใจคอมโพเนนต์ของชุดข้อมูลเวลาด้วย "Seasonal and Trend decomposition โดยใช้ Loess" | [แผนภูมิ Time series forecasting](https://github.com/Microsoft/powerbi-visuals-forcasting-exp/) </br>ใช้วิธี exponential smoothing เพื่อคาดการณ์ค่าอนาคตตามค่าที่ได้รับก่อนหน้านี้

## <a name="next-steps"></a>ขั้นตอนถัดไป

หากต้องการลองสร้างวิชวล Power BI โปรดดู [การพัฒนาวิชวลการ์ดวงกลมใน Power BI](develop-circle-card.md)
