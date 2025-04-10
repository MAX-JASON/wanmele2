```html
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>國泰壽險產品投資效益分析報告</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            padding: 15px;
            max-width: 100%;
        }
        h1, h2, h3 {
            margin: 15px 0;
            color: #336699;
        }
        h1 {
            font-size: 24px;
        }
        h2 {
            font-size: 20px;
            margin-top: 25px;
        }
        h3 {
            font-size: 18px;
        }
        p {
            margin-bottom: 15px;
        }
        .info-box {
            background-color: #f5f5f5;
            padding: 15px;
            border-radius: 5px;
            margin: 15px 0;
        }
        .highlight-box {
            background-color: #e6f7ff;
            padding: 15px;
            border-radius: 5px;
            margin: 15px 0;
        }
        .product-table {
            width: 100%;
            border-collapse: collapse;
            margin: 15px 0;
            font-size: 14px;
        }
        .product-table th,
        .product-table td {
            padding: 8px;
            text-align: left;
            border: 1px solid #ddd;
        }
        .product-table th {
            background-color: #eef6ff;
        }
        .product-row-highlight {
            background-color: #f0f9ed;
        }
        .compare-row {
            background-color: #fff2e6;
        }
        .data-table {
            width: 100%;
            border-collapse: collapse;
            margin: 15px 0;
            font-size: 13px;
            overflow-x: auto;
            display: block;
        }
        .data-table th,
        .data-table td {
            padding: 6px 4px;
            text-align: left;
            border: 1px solid #ddd;
        }
        .data-table th {
            background-color: #eef6ff;
        }
        .chart-container {
            margin: 25px 0;
            padding: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .chart-title {
            text-align: center;
            margin-bottom: 10px;
        }
        .chart-subtitle {
            text-align: center;
            font-size: 14px;
            color: #666;
            margin-bottom: 20px;
        }
        .bar-chart {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin: 20px 0;
        }
        .bar-group {
            display: flex;
            flex-direction: column;
            gap: 5px;
        }
        .bar-label {
            display: flex;
            justify-content: space-between;
        }
        .bar-container {
            height: 25px;
            background-color: #eee;
            border-radius: 4px;
            overflow: hidden;
        }
        .bar {
            height: 100%;
            background-color: #6c9bcf;
        }
        .bar-2 {
            background-color: #93c47d;
        }
        .legend {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }
        .legend-item {
            display: flex;
            align-items: center;
            gap: 5px;
        }
        .legend-color {
            width: 20px;
            height: 15px;
        }
        .premium-chart {
            margin-top: 25px;
        }
        .premium-bar {
            margin: 15px 0;
        }
        .premium-bar-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }
        .premium-bar-container {
            height: 25px;
            background-color: #eee;
            border-radius: 4px;
            overflow: hidden;
        }
        .premium-bar-fill {
            height: 100%;
            background-color: #5b9bd5;
        }
        .strong {
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>國泰壽險產品投資效益分析報告</h1>
    <h2>添美多與萬美利 投資組合價值分析</h2>

    <div class="info-box">
        <p><strong>案例參數設定：</strong></p>
        <ul style="padding-left: 20px;">
            <li>投保主體：55歲被保險人（民國101年9月初始承保）</li>
            <li>保費結構：兩案均採年繳USD 3,178，6年期繳費，總計USD 19,068</li>
            <li>宣告利率：添美多3.25% p.a.（適用期間：民國101年至今）vs. 萬美利4.5% p.a.（現行）</li>
            <li>分析指標：內部報酬率(IRR)、名目報酬(Nominal Return)、風險調整後報酬(Risk-Adjusted Return)</li>
            <li>評估區間：最長20年期資產價值與保障累積效益比較</li>
            <li>現況說明：添美多當前保單價值已累積至USD 25,000</li>
        </ul>
    </div>

    <h2>保單技術參數比較</h2>

    <div style="overflow-x: auto;">
        <table class="product-table">
            <tr>
                <th>保單</th>
                <th>產品屬性</th>
                <th>年繳保費</th>
                <th>繳費期間</th>
                <th>總保費</th>
                <th>現行利率</th>
                <th>產品特性</th>
            </tr>
            <tr>
                <td>添美多</td>
                <td>利率變動型壽險</td>
                <td>$3,178</td>
                <td>6年</td>
                <td>$19,068</td>
                <td>3.25%</td>
                <td>第一代美元計價利率敏感型保單，含保費分離設計</td>
            </tr>
            <tr class="product-row-highlight">
                <td>萬美利</td>
                <td>利率變動型壽險</td>
                <td>$3,178</td>
                <td>6年</td>
                <td>$19,068</td>
                <td>4.5%</td>
                <td>新世代美元計價壽險，具動態增值機制與最低保證利率</td>
            </tr>
            <tr class="compare-row">
                <td>差異/比較</td>
                <td>相同類別</td>
                <td>相同</td>
                <td>相同</td>
                <td>相同</td>
                <td>+115 bps</td>
                <td>萬美利提供更高利差回饋，中長期複利效應優越</td>
            </tr>
        </table>
    </div>

    <div class="highlight-box">
        <p><strong>現況評估與未來展望：</strong></p>
        <p>添美多保單目前已累積至$25,000的現金價值，展現了多年來的穩健增值。然而，萬美利的115個基點利率優勢預計在未來20年內將創造更顯著的增值差異。在相同投入成本結構下，萬美利的複利效應優勢將隨時間逐漸擴大，特別是在10年後的中長期階段。</p>
    </div>

    <h2>添美多vs萬美利 內部報酬率與現金價值比較</h2>

    <div style="overflow-x: auto;">
        <table class="data-table">
            <tr>
                <th>經過年度</th>
                <th>添美多現金價值</th>
                <th>添美多IRR</th>
                <th>萬美利現金價值</th>
                <th>萬美利IRR</th>
                <th>價值差額</th>
                <th>IRR差異</th>
            </tr>
            <tr class="compare-row">
                <td>現況</td>
                <td><strong>$25,000</strong></td>
                <td>1.8%</td>
                <td>-</td>
                <td>-</td>
                <td>-</td>
                <td>-</td>
            </tr>
            <tr>
                <td>未來1年</td>
                <td>$25,812</td>
                <td>1.9%</td>
                <td>$26,100</td>
                <td>2.3%</td>
                <td>+$288</td>
                <td>+0.4%</td>
            </tr>
            <tr>
                <td>未來3年</td>
                <td>$27,510</td>
                <td>2.0%</td>
                <td>$28,450</td>
                <td>2.6%</td>
                <td>+$940</td>
                <td>+0.6%</td>
            </tr>
            <tr>
                <td>未來5年</td>
                <td>$29,340</td>
                <td>2.1%</td>
                <td>$31,050</td>
                <td>2.8%</td>
                <td>+$1,710</td>
                <td>+0.7%</td>
            </tr>
            <tr class="product-row-highlight">
                <td>未來10年</td>
                <td>$34,430</td>
                <td>2.2%</td>
                <td><strong>$38,530</strong></td>
                <td><strong>3.1%</strong></td>
                <td><strong>+$4,100</strong></td>
                <td><strong>+0.9%</strong></td>
            </tr>
            <tr class="product-row-highlight">
                <td>未來15年</td>
                <td>$40,420</td>
                <td>2.3%</td>
                <td><strong>$47,840</strong></td>
                <td><strong>3.3%</strong></td>
                <td><strong>+$7,420</strong></td>
                <td><strong>+1.0%</strong></td>
            </tr>
            <tr class="compare-row">
                <td>未來20年</td>
                <td>$47,440</td>
                <td>2.4%</td>
                <td><strong>$59,530</strong></td>
                <td><strong>3.4%</strong></td>
                <td><strong>+$12,090</strong></td>
                <td><strong>+1.0%</strong></td>
            </tr>
        </table>
    </div>

    <div class="highlight-box">
        <p><strong>中長期投資效益分析：</strong></p>
        <p>以添美多目前$25,000的現金價值為基礎，未來20年內兩產品展現了顯著的績效差異。萬美利在20年後可望達到$59,530的現金價值，較添美多元的$47,440高出$12,090（增幅25.5%）。IRR差異雖僅約1.0個百分點（3.4% vs 2.4%），但透過複利效應所創造的實際金額差距相當可觀。值得注意的是，差距從第10年開始明顯擴大，反映了利率優勢在中長期的顯著影響。</p>
    </div>

    <h2>現金價值積累率分析</h2>

    <div class="chart-container">
        <h3 class="chart-title">投入資本比率(Cash Value/Premium Ratio)</h3>
        <div class="chart-subtitle">衡量每$1美元保費轉換為保單現金價值的效率</div>
        
        <div class="bar-chart">
            <div class="bar-group">
                <div class="bar-label">
                    <span>現況</span>
                    <span>1.31x/--</span>
                </div>
                <div class="bar-container">
                    <div class="bar" style="width: 38%;"></div>
                </div>
            </div>
            
            <div class="bar-group">
                <div class="bar-label">
                    <span>5年</span>
                    <span>1.54x/1.63x</span>
                </div>
                <div style="display: flex;">
                    <div class="bar-container" style="width: 48%;">
                        <div class="bar" style="width: 44%;"></div>
                    </div>
                    <div class="bar-container" style="width: 48%; margin-left: 4%;">
                        <div class="bar bar-2" style="width: 47%;"></div>
                    </div>
                </div>
            </div>
            
            <div class="bar-group">
                <div class="bar-label">
                    <span>10年</span>
                    <span>1.80x/2.02x</span>
                </div>
                <div style="display: flex;">
                    <div class="bar-container" style="width: 48%;">
                        <div class="bar" style="width: 51%;"></div>
                    </div>
                    <div class="bar-container" style="width: 48%; margin-left: 4%;">
                        <div class="bar bar-2" style="width: 58%;"></div>
                    </div>
                </div>
            </div>
            
            <div class="bar-group">
                <div class="bar-label">
                    <span>15年</span>
                    <span>2.12x/2.51x</span>
                </div>
                <div style="display: flex;">
                    <div class="bar-container" style="width: 48%;">
                        <div class="bar" style="width: 61%;"></div>
                    </div>
                    <div class="bar-container" style="width: 48%; margin-left: 4%;">
                        <div class="bar bar-2" style="width: 72%;"></div>
                    </div>
                </div>
            </div>
            
            <div class="bar-group">
                <div class="bar-label">
                    <span>20年</span>
                    <span>2.49x/3.12x</span>
                </div>
                <div style="display: flex;">
                    <div class="bar-container" style="width: 48%;">
                        <div class="bar" style="width: 71%;"></div>
                    </div>
                    <div class="bar-container" style="width: 48%; margin-left: 4%;">
                        <div class="bar bar-2" style="width: 89%;"></div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="legend">
            <div class="legend-item">
                <div class="legend-color" style="background-color: #6c9bcf;"></div>
                <span>添美多</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background-color: #93c47d;"></div>
                <span>萬美利</span>
            </div>
        </div>
        
        <div style="margin-top: 20px; font-size: 14px; color: #555;">
            <p><strong>積累效率分析：</strong> 比較每$1美元保費所累積的現金價值，萬美利在20年期間可將保費轉化為3.12倍的現金價值，顯著高於添美多的2.49倍。此分析顯示萬美利的資金轉換效率隨時間遞增，提供更高的保費價值回報。保費價值轉換倍率的差距從10年後開始顯著擴大，反映利率優勢的長期累積效應。</p>
        </div>
    </div>

    <h2>萬美利相較添美多的現金價值溢價率分析</h2>

    <div class="chart-container">
        <h3 class="chart-title">萬美利現金價值溢價率發展趨勢</h3>
        <div class="chart-subtitle">溢價率計算方法: [(萬美利現金價值 - 添美多現金價值) / 添美多元現金價值] × 100%</div>
        
        <div class="premium-chart">
            <div class="premium-bar">
                <div class="premium-bar-label">
                    <span>1年</span>
                    <span>1.1%</span>
                </div>
                <div class="premium-bar-container">
                    <div class="premium-bar-fill" style="width: 4%;"></div>
                </div>
            </div>
            
            <div class="premium-bar">
                <div class="premium-bar-label">
                    <span>3年</span>
                    <span>3.4%</span>
                </div>
                <div class="premium-bar-container">
                    <div class="premium-bar-fill" style="width: 11%;"></div>
                </div>
            </div>
            
            <div class="premium-bar">
                <div class="premium-bar-label">
                    <span>5年</span>
                    <span>5.8%</span>
                </div>
                <div class="premium-bar-container">
                    <div class="premium-bar-fill" style="width: 19%;"></div>
                </div>
            </div>
            
            <div class="premium-bar">
                <div class="premium-bar-label">
                    <span>10年</span>
                    <span>11.9%</span>
                </div>
                <div class="premium-bar-container">
                    <div class="premium-bar-fill" style="width: 40%;"></div>
                </div>
            </div>
            
            <div class="premium-bar">
                <div class="premium-bar-label">
                    <span>15年</span>
                    <span>18.4%</span>
                </div>
                <div class="premium-bar-container">
                    <div class="premium-bar-fill" style="width: 61%;"></div>
                </div>
            </div>
            
            <div class="premium-bar">
                <div class="premium-bar-label">
                    <span>20年</span>
                    <span>25.5%</span>
                </div>
                <div class="premium-bar-container">
                    <div class="premium-bar-fill" style="width: 85%;"></div>
                </div>
            </div>
        </div>
        
        <div style="margin-top: 20px; font-size: 14px; color: #555;">
            <p>值得注意的是溢價率呈現加速上升趨勢，反映複利效應隨時間增強的特性。溢價率從最初1年的1.1%增長至20年後的25.5%，顯示長期投資的複利優勢。</p>
        </div>
    </div>
</body>
</html>
