---
title: 券商费率对比
author: 老倔驴
date: 2025-03-10
category: 1
layout: post
---

## 券商费率对比表

下表汇总了各大券商的交易费率信息，帮助您选择最适合的开户方案：

<div class="table-responsive">
  <table id="brokerTable" class="table table-striped table-bordered">
    <thead>
      <tr>
        <th>代号</th>
        <th>券商</th>
        <th>入金门槛</th>
        <th>股票</th>
        <th>过户费</th>
        <th>ETF</th>
        <th>逆回购</th>
        <th>可转债</th>
        <th>软件支持</th>
        <th>永久费率要求</th>
      </tr>
    </thead>
    <tbody></tbody>
  </table>
</div>

<script>
// 数据定义
const brokerData = [
    {
        "代号": "01号",
        "券商": "国S\n江西国资首家上市 ",
        "入金门槛": "1.5w",
        "股票": "万0.854 兔5\n1元起",
        "过户费": "沪万0.1,深免",
        "ETF": "万0.5兔5 \n1元起",
        "逆回购": "1折",
        "可转债": "万0.5兔5 \n1元起",
        "软件支持": "✅同花顺 \n✅通达信",
        "永久费率要求": "入金1.5W，保持20个交易日，且股票类交易至少一次"
    },
    {
        "代号": "02号",
        "券商": "CC\n费率最低",
        "入金门槛": "1.5w",
        "股票": "万0.75兔5\n1元起",
        "过户费": "沪深万0.1",
        "ETF": "万0.5兔5\n0.1元起",
        "逆回购": "1折",
        "可转债": "沪万0.44\n深万0.8兔5 \n0.5起",
        "软件支持": "✅同花顺 \n✅通达信",
        "永久费率要求": "入金1.5W，保持2个月，日均资产不低于1.3W，自动转永久"
    },
    {
        "代号": "03号",
        "券商": "银H\n头部券商",
        "入金门槛": "1.5w",
        "股票": "万0.854 \n5元起步",
        "过户费": "沪万0.1,深免",
        "ETF": "万0.5 免5\n0.01起",
        "逆回购": "1折",
        "可转债": "万0.5 , 5元起",
        "软件支持": "✅同花顺 \n✅通达信",
        "永久费率要求": "入金1.5万以上，月日均资产1.5W以上(连续保持2个月)，且交易2000以上股票或者权益类ETF稳妥达标!自动转永久低佣!!"
    },
    {
        "代号": "04号",
        "券商": "华T \n头部券商 APP好用",
        "入金门槛": "1.5w",
        "股票": "万1.154",
        "过户费": "沪万0.1,深免",
        "ETF": "万 1",
        "逆回购": "1折",
        "可转债": "万0.4 免5",
        "软件支持": "✅同花顺 \n✅通达信",
        "永久费率要求": "入金1.5W，30日保持活跃，累计偏股型交易额累计1W"
    },
    {
        "代号": "10号",
        "券商": "国 J \n50w开量化",
        "入金门槛": "30w",
        "股票": "0.854",
        "过户费": "沪万0.1,深免",
        "ETF": "万0.5棉5 \n0.5起",
        "逆回购": "1折",
        "可转债": "万0.5 0.1 元起",
        "软件支持": "✅同花顺 \n✅通达信PC",
        "永久费率要求": "入金30w起,保持3个半月，股票持仓5成。 (入金50W送永久Level2,独立高速通道，送量化QMT和Ptrade)"
    },
    {
        "代号": "11号",
        "券商": "国T\n头部券商",
        "入金门槛": "50w",
        "股票": "万0.85免五\n0元起",
        "过户费": "沪万0.1,深免",
        "ETF": "万0.5兔五\n0.01元起",
        "逆回购": "1折",
        "可转债": "万0.6， 0.1起",
        "软件支持": "✅同花顺 \n✅通达信PC",
        "永久费率要求": "入金50W，保持3个月，自动转永久。必须首开"
    },
    {
        "代号": "12号",
        "券商": "长J \n腰部 国企上市",
        "入金门槛": "30w",
        "股票": "万0.854M5 \n0元起",
        "过户费": "沪深万0.1",
        "ETF": "万0.6M5 \n0元起",
        "逆回购": "1折",
        "可转债": "万0.5M5 0元起",
        "软件支持": "✅同花顺",
        "永久费率要求": "入金30W，保持30日，最少一次股票型交易。 (北交所万2.25M5，港股通万1M5,新客理财，5万/10万固定年化6%)"
    },
    {
        "代号": "13号",
        "券商": "H * \n送半年 L2 国企上市",
        "入金门槛": "20w",
        "股票": "万0.85兔5 \n0.01元起",
        "过户费": "沪万0.1,深免",
        "ETF": "万0.5兔5 \n0.01元起",
        "逆回购": "1折",
        "可转债": "万0.5兔5 \n沪1深0.01起",
        "软件支持": "✅手机同花顺 \n✅手机通达信",
        "永久费率要求": "入金20W，月内至少一次8成仓位获得永久费率优惠。北交所万2M5，港股通万1不免5，期权2元（四川身份证不能开）"
    }
];

// 渲染表格函数
function renderBrokerTable() {
    const tableBody = document.querySelector('#brokerTable tbody');
    tableBody.innerHTML = '';
    
    brokerData.forEach(broker => {
        const row = document.createElement('tr');
        
        // 获取表头的列名
        const headers = ['代号', '券商', '入金门槛', '股票', '过户费', 'ETF', '逆回购', '可转债', '软件支持', '永久费率要求'];
        
        headers.forEach(header => {
            const cell = document.createElement('td');
            // 将换行符转换为<br>标签
            cell.innerHTML = broker[header].replace(/\n/g, '<br>');
            row.appendChild(cell);
        });
        
        tableBody.appendChild(row);
    });
}

// 页面加载完成后渲染表格
document.addEventListener('DOMContentLoaded', function() {
    renderBrokerTable();
    
    // 添加表格样式
    const style = document.createElement('style');
    style.textContent = `
        .table-responsive {
            overflow-x: auto;
            margin: 20px 0;
        }
        .table {
            width: 100%;
            border-collapse: collapse;
            font-size: 14px;
        }
        .table th, .table td {
            padding: 12px;
            text-align: left;
            border: 1px solid #ddd;
            vertical-align: top;
        }
        .table th {
            background-color: #f8f8f8;
            font-weight: bold;
            white-space: nowrap;
        }
        .table tr:nth-child(even) {
            background-color: #f9f9f9;
        }
        .table tr:hover {
            background-color: #f1f1f1;
        }
        /* 针对移动设备的响应式设计 */
        @media (max-width: 768px) {
            .table th, .table td {
                padding: 8px;
                font-size: 12px;
            }
        }
    `;
    document.head.appendChild(style);
});
</script>

## 免责声明

* 以上费率信息仅供参考，实际费率以券商官方公布为准。
* 各项优惠政策可能会根据券商规定随时调整，请在开户前与客户经理确认最新费率。
* 投资有风险，入市需谨慎。

如果您有开户需求或想了解更多详情，请联系我们：

**优惠开户:**  304278785 (QQ) netqqnet (wechat)
**券商合作:**  qing606#gmail.com