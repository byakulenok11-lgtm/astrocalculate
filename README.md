<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Анализ лидов и ROI — Астрология / Нумерология КЗ</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: 'Segoe UI', Arial, sans-serif; background: #0F1322; color: #E8EDF5; min-height: 100vh; padding: 24px; }

  h1 { font-size: 26px; font-weight: 800; color: #fff; margin-bottom: 4px; }
  .subtitle { font-size: 13px; color: #7A90B0; margin-bottom: 28px; }

  .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 18px; margin-bottom: 24px; }
  .grid-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 16px; margin-bottom: 24px; }
  .grid-full { margin-bottom: 24px; }

  .card { background: #1A2035; border-radius: 14px; padding: 20px; border: 1px solid #252E48; }
  .card-blue { border-color: #1E90FF; }
  .card-green { border-color: #18A86B; }
  .card-orange { border-color: #E5820A; }
  .card-pink { border-color: #E53E8C; }

  .card-title { font-size: 11px; font-weight: 700; text-transform: uppercase; letter-spacing: 1px; color: #7A90B0; margin-bottom: 14px; }

  label { display: block; font-size: 12px; color: #9AAAC0; margin-bottom: 5px; margin-top: 12px; }
  label:first-of-type { margin-top: 0; }

  input[type=range] { width: 100%; accent-color: #1E90FF; cursor: pointer; }
  .range-row { display: flex; align-items: center; gap: 10px; }
  .range-val { font-size: 15px; font-weight: 700; color: #1E90FF; min-width: 90px; text-align: right; }

  select { background: #252E48; border: 1px solid #353E58; color: #E8EDF5; padding: 7px 10px; border-radius: 8px; font-size: 13px; width: 100%; cursor: pointer; }

  .big-num { font-size: 36px; font-weight: 900; line-height: 1; }
  .big-label { font-size: 12px; color: #7A90B0; margin-top: 4px; }
  .blue { color: #1E90FF; }
  .green { color: #18A86B; }
  .orange { color: #E5820A; }
  .pink { color: #E53E8C; }
  .white { color: #fff; }
  .red { color: #E53E50; }

  .kpi-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 14px; margin-bottom: 24px; }
  .kpi { background: #1A2035; border-radius: 12px; padding: 16px; border: 1px solid #252E48; text-align: center; }

  .scenario-tabs { display: flex; gap: 10px; margin-bottom: 18px; }
  .tab { padding: 8px 18px; border-radius: 20px; font-size: 13px; font-weight: 600; cursor: pointer; border: 1.5px solid #252E48; background: #1A2035; color: #7A90B0; transition: all 0.2s; }
  .tab.active { background: #1E90FF; border-color: #1E90FF; color: #fff; }

  table { width: 100%; border-collapse: collapse; font-size: 13px; }
  th { background: #1E90FF; color: #fff; padding: 10px 12px; text-align: left; font-weight: 600; }
  td { padding: 9px 12px; border-bottom: 1px solid #252E48; }
  tr:nth-child(even) td { background: #161E30; }
  tr:hover td { background: #1E2A40; }
  .td-right { text-align: right; font-weight: 600; }
  .tag { display: inline-block; padding: 2px 9px; border-radius: 10px; font-size: 11px; font-weight: 700; }
  .tag-green { background: #0D3D28; color: #18A86B; }
  .tag-blue { background: #0B1E3D; color: #1E90FF; }
  .tag-orange { background: #3D2200; color: #E5820A; }

  .funnel { display: flex; gap: 0; align-items: stretch; margin: 14px 0; }
  .funnel-step { flex: 1; background: #1A2035; border: 1px solid #252E48; padding: 14px 10px; text-align: center; position: relative; }
  .funnel-step:not(:last-child)::after { content: '→'; position: absolute; right: -10px; top: 50%; transform: translateY(-50%); color: #1E90FF; font-size: 18px; z-index: 2; }
  .funnel-num { font-size: 22px; font-weight: 900; }
  .funnel-lbl { font-size: 10px; color: #7A90B0; margin-top: 4px; }

  .alert { background: #0D1830; border: 1px solid #1E90FF; border-radius: 10px; padding: 14px 16px; font-size: 13px; color: #B0C4E0; line-height: 1.6; }
  .alert strong { color: #fff; }

  .bar-row { display: flex; align-items: center; gap: 10px; margin-bottom: 8px; }
  .bar-label { width: 140px; font-size: 12px; color: #9AAAC0; flex-shrink: 0; }
  .bar-bg { flex: 1; background: #252E48; border-radius: 4px; height: 20px; overflow: hidden; }
  .bar-fill { height: 100%; border-radius: 4px; transition: width 0.4s; display: flex; align-items: center; padding-left: 8px; font-size: 11px; font-weight: 700; color: #fff; }
  .bar-val { width: 80px; text-align: right; font-size: 13px; font-weight: 700; }

  .month-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 14px; }
  .month-card { background: #1A2035; border-radius: 12px; padding: 16px; border-top: 4px solid; }

  @media (max-width: 720px) {
    .grid, .grid-3, .kpi-grid, .month-grid { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>

<h1>📊 Анализ стоимости лида и ROI</h1>
<p class="subtitle">Ниша: Астрология · Нумерология · Ба Цзы · Ци Мэнь — Казахстан (Алматы / Астана) · Meta Ads Instagram</p>

<!-- SCENARIO TABS -->
<div class="scenario-tabs">
  <div class="tab active" onclick="setScenario('start')">🟡 Старт</div>
  <div class="tab" onclick="setScenario('mid')">🟢 Рост</div>
  <div class="tab" onclick="setScenario('scale')">🔵 Масштаб</div>
</div>

<!-- CONTROLS -->
<div class="grid">
  <div class="card">
    <div class="card-title">⚙️ Рекламный бюджет</div>
    <label>Бюджет в месяц (₸)</label>
    <div class="range-row">
      <input type="range" id="budget" min="20000" max="300000" step="5000" value="40000" oninput="update()">
      <span class="range-val blue" id="budgetVal">40 000 ₸</span>
    </div>
    <label>Цена лида — CPL (₸)</label>
    <div class="range-row">
      <input type="range" id="cpl" min="1000" max="15000" step="500" value="3500" oninput="update()">
      <span class="range-val blue" id="cplVal">3 500 ₸</span>
    </div>
    <label>Конверсия лид → продажа (%)</label>
    <div class="range-row">
      <input type="range" id="conv" min="5" max="60" step="1" value="20" oninput="update()">
      <span class="range-val green" id="convVal">20%</span>
    </div>
  </div>

  <div class="card">
    <div class="card-title">💰 Услуги и средний чек</div>
    <label>Основная продаваемая услуга</label>
    <select id="service" onchange="update()">
      <option value="20000">Один вопрос — 20 000 ₸</option>
      <option value="35000" selected>Нумерология — 35 000 ₸</option>
      <option value="50000">Ба Цзы + Нумерология — 50 000 ₸</option>
      <option value="80000">Ци Мэнь + Нумерология — 80 000 ₸</option>
      <option value="45000">Карта ребёнка — 45 000 ₸</option>
    </select>
    <label>Апсейл (%): доля клиентов, берущих дороже</label>
    <div class="range-row">
      <input type="range" id="upsell" min="0" max="60" step="5" value="20" oninput="update()">
      <span class="range-val orange" id="upsellVal">20%</span>
    </div>
    <label>Доля органических клиентов (без рекламы, %)</label>
    <div class="range-row">
      <input type="range" id="organic" min="0" max="80" step="5" value="20" oninput="update()">
      <span class="range-val" style="color:#C974FF" id="organicVal">20%</span>
    </div>
  </div>
</div>

<!-- MAIN KPIs -->
<div class="kpi-grid" id="kpis"></div>

<!-- FUNNEL -->
<div class="card grid-full">
  <div class="card-title">🔽 Воронка — визуализация</div>
  <div class="funnel" id="funnel"></div>
</div>

<!-- CHARTS + TABLE -->
<div class="grid">
  <div class="card">
    <div class="card-title">📦 Юнит-экономика одной продажи</div>
    <div id="unitBars"></div>
  </div>
  <div class="card">
    <div class="card-title">📋 Допустимые CPL по услугам</div>
    <table id="cplTable"></table>
  </div>
</div>

<!-- MONTHS -->
<div class="card grid-full">
  <div class="card-title">📅 Прогноз по месяцам (3 сценария)</div>
  <div class="month-grid" id="months"></div>
</div>

<!-- ALERT -->
<div class="alert" id="alertBox"></div>

<script>
const FMT = n => Math.round(n).toLocaleString('ru-RU');
const FMT_PCT = n => n.toFixed(1) + '%';

const SCENARIOS = {
  start: { budget: 40000, cpl: 4000, conv: 15, service: '35000', upsell: 15, organic: 15 },
  mid:   { budget: 80000, cpl: 3000, conv: 22, service: '50000', upsell: 25, organic: 20 },
  scale: { budget: 150000, cpl: 2500, conv: 28, service: '65000', upsell: 30, organic: 25 },
};

function setScenario(key) {
  const s = SCENARIOS[key];
  document.getElementById('budget').value = s.budget;
  document.getElementById('cpl').value = s.cpl;
  document.getElementById('conv').value = s.conv;
  document.getElementById('service').value = s.service;
  document.getElementById('upsell').value = s.upsell;
  document.getElementById('organic').value = s.organic;
  document.querySelectorAll('.tab').forEach((t,i) => t.classList.toggle('active', ['start','mid','scale'][i] === key));
  update();
}

function update() {
  const budget = +document.getElementById('budget').value;
  const cpl = +document.getElementById('cpl').value;
  const conv = +document.getElementById('conv').value / 100;
  const servicePrice = +document.getElementById('service').value;
  const upsellPct = +document.getElementById('upsell').value / 100;
  const organicPct = +document.getElementById('organic').value / 100;

  // Update labels
  document.getElementById('budgetVal').textContent = FMT(budget) + ' ₸';
  document.getElementById('cplVal').textContent = FMT(cpl) + ' ₸';
  document.getElementById('convVal').textContent = FMT_PCT(conv * 100);
  document.getElementById('upsellVal').textContent = FMT_PCT(upsellPct * 100);
  document.getElementById('organicVal').textContent = FMT_PCT(organicPct * 100);

  // Core calculations
  const leadsFromAds = Math.floor(budget / cpl);
  const salesFromAds = Math.floor(leadsFromAds * conv);
  const upsellPrice = servicePrice * 1.8; // апсейл = более дорогая услуга (+80%)
  const avgCheck = servicePrice * (1 - upsellPct) + upsellPrice * upsellPct;
  const revenueFromAds = salesFromAds * avgCheck;

  // Organic bonus
  const organicSales = Math.floor(salesFromAds * organicPct);
  const organicRevenue = organicSales * avgCheck;

  const totalSales = salesFromAds + organicSales;
  const totalRevenue = revenueFromAds + organicRevenue;
  const profit = totalRevenue - budget;
  const roas = totalRevenue / budget;
  const cac = budget / (salesFromAds || 1); // cost per customer (ads only)
  const roi = ((totalRevenue - budget) / budget) * 100;

  // KPIs
  const kpiData = [
    { val: FMT(leadsFromAds), lbl: 'Лидов с рекламы', color: 'blue' },
    { val: FMT(totalSales), lbl: 'Продаж (реклама + органика)', color: 'green' },
    { val: FMT(Math.round(avgCheck)) + ' ₸', lbl: 'Средний чек', color: 'orange' },
    { val: FMT(Math.round(totalRevenue)) + ' ₸', lbl: 'Выручка в месяц', color: 'pink' },
    { val: FMT(Math.round(profit)) + ' ₸', lbl: 'Прибыль (доход − реклама)', color: profit >= 0 ? 'green' : 'red' },
    { val: roas.toFixed(2) + 'x', lbl: 'ROAS (возврат на бюджет)', color: roas >= 3 ? 'green' : roas >= 2 ? 'orange' : 'red' },
    { val: FMT(Math.round(cac)) + ' ₸', lbl: 'CAC (стоимость клиента)', color: 'blue' },
    { val: FMT_PCT(roi), lbl: 'ROI рекламного бюджета', color: roi >= 100 ? 'green' : roi >= 50 ? 'orange' : 'red' },
  ];

  document.getElementById('kpis').innerHTML = kpiData.map(k => `
    <div class="kpi">
      <div class="big-num ${k.color}">${k.val}</div>
      <div class="big-label">${k.lbl}</div>
    </div>
  `).join('');

  // Funnel
  const impressions = Math.floor(budget / 0.35); // CPM ~350₸ → impression count
  const clicks = Math.floor(impressions * 0.018); // CTR ~1.8%
  document.getElementById('funnel').innerHTML = [
    { num: FMT(impressions), lbl: 'Показов', color: '#7A90B0' },
    { num: FMT(clicks), lbl: 'Кликов', color: '#6B7CB5' },
    { num: FMT(leadsFromAds), lbl: 'Лидов', color: '#1E90FF' },
    { num: FMT(salesFromAds), lbl: 'Продаж (реклама)', color: '#18A86B' },
    { num: FMT(totalSales), lbl: 'Итого клиентов', color: '#E5820A' },
  ].map((s, i) => `
    <div class="funnel-step" style="border-top: 3px solid ${s.color}">
      <div class="funnel-num" style="color:${s.color}">${s.num}</div>
      <div class="funnel-lbl">${s.lbl}</div>
    </div>
  `).join('');

  // Unit bars
  const maxRev = servicePrice;
  const adCostPerSale = cac;
  const grossMargin = avgCheck - adCostPerSale;
  const barsData = [
    { lbl: 'Цена услуги', val: servicePrice, max: avgCheck * 1.2, color: '#1E90FF' },
    { lbl: 'Средний чек (с апс.)', val: Math.round(avgCheck), max: avgCheck * 1.2, color: '#6B50FF' },
    { lbl: 'Затраты на рекламу/клиента', val: Math.round(adCostPerSale), max: avgCheck * 1.2, color: '#E5820A' },
    { lbl: 'Маржа (чек − реклама)', val: Math.round(grossMargin), max: avgCheck * 1.2, color: grossMargin > 0 ? '#18A86B' : '#E53E50' },
  ];

  document.getElementById('unitBars').innerHTML = barsData.map(b => {
    const w = Math.max(0, Math.min(100, (b.val / b.max) * 100));
    return `
      <div class="bar-row">
        <div class="bar-label">${b.lbl}</div>
        <div class="bar-bg">
          <div class="bar-fill" style="width:${w}%; background:${b.color}">${FMT(b.val)} ₸</div>
        </div>
      </div>
    `;
  }).join('');

  // CPL table
  const services = [
    { name: 'Один вопрос', price: 20000, tag: 'Вход' },
    { name: 'Нумерология', price: 35000, tag: '' },
    { name: 'Ба Цзы + Нум.', price: 50000, tag: '' },
    { name: 'Ци Мэнь + Нум.', price: 80000, tag: 'Флагман' },
    { name: 'Карта ребёнка', price: 45000, tag: 'Новый' },
  ];

  const tableRows = services.map(sv => {
    const maxCpl = Math.floor(sv.price * conv * 0.4); // не более 40% маржи от выручки
    const ok = cpl <= maxCpl;
    const tagHtml = sv.tag ? `<span class="tag ${sv.tag === 'Флагман' ? 'tag-orange' : 'tag-blue'}">${sv.tag}</span>` : '';
    return `<tr>
      <td>${sv.name} ${tagHtml}</td>
      <td class="td-right">${FMT(sv.price)} ₸</td>
      <td class="td-right">${FMT(maxCpl)} ₸</td>
      <td class="td-right" style="color:${ok ? '#18A86B' : '#E53E50'}; font-weight:700">${ok ? '✓ ОК' : '✗ Дорого'}</td>
    </tr>`;
  }).join('');

  document.getElementById('cplTable').innerHTML = `
    <thead><tr><th>Услуга</th><th>Цена</th><th>Макс. CPL</th><th>Статус</th></tr></thead>
    <tbody>${tableRows}</tbody>
  `;

  // Monthly forecast
  const m1 = { budget: budget * 0.8, cpl: cpl * 1.15, conv: conv * 0.9 };
  const m2 = { budget: budget, cpl: cpl, conv: conv };
  const m3 = { budget: budget * 1.3, cpl: cpl * 0.85, conv: conv * 1.1 };

  function calcMonth(m, label, color) {
    const leads = Math.floor(m.budget / m.cpl);
    const sales = Math.floor(leads * m.conv) + Math.floor(leads * m.conv * organicPct);
    const rev = Math.round(sales * avgCheck);
    const pr = rev - Math.round(m.budget);
    return `
      <div class="month-card" style="border-color:${color}">
        <div style="font-size:12px; font-weight:700; color:${color}; margin-bottom:12px; text-transform:uppercase">${label}</div>
        <div style="display:grid; grid-template-columns:1fr 1fr; gap:8px">
          <div><div style="font-size:11px; color:#7A90B0">Бюджет</div><div style="font-weight:700; font-size:14px">${FMT(Math.round(m.budget))} ₸</div></div>
          <div><div style="font-size:11px; color:#7A90B0">Лидов</div><div style="font-weight:700; font-size:14px; color:#1E90FF">${FMT(leads)}</div></div>
          <div><div style="font-size:11px; color:#7A90B0">Продаж</div><div style="font-weight:700; font-size:14px; color:#18A86B">${FMT(sales)}</div></div>
          <div><div style="font-size:11px; color:#7A90B0">Выручка</div><div style="font-weight:700; font-size:14px; color:${color}">${FMT(rev)} ₸</div></div>
          <div style="grid-column:span 2"><div style="font-size:11px; color:#7A90B0">Прибыль (≈ без себест.)</div>
          <div style="font-weight:900; font-size:18px; color:${pr >= 0 ? '#18A86B' : '#E53E50'}">${pr >= 0 ? '+' : ''}${FMT(pr)} ₸</div></div>
        </div>
      </div>
    `;
  }

  document.getElementById('months').innerHTML =
    calcMonth(m1, '📅 Месяц 1 (тест)', '#E5820A') +
    calcMonth(m2, '📅 Месяц 2 (оптимум)', '#1E90FF') +
    calcMonth(m3, '📅 Месяц 3 (масштаб)', '#18A86B');

  // Alert
  let msg = '';
  if (roi < 100) {
    msg = `⚠️ <strong>Осторожно:</strong> При текущем CPL ${FMT(cpl)} ₸ и конверсии ${FMT_PCT(conv*100)} ROI ниже 100%. Рекомендуем снизить CPL через улучшение креативов или поднять конверсию через квалификацию в Direct.`;
  } else if (cac > servicePrice * 0.4) {
    msg = `⚡ <strong>Обратите внимание:</strong> Стоимость привлечения клиента (${FMT(Math.round(cac))} ₸) составляет более 40% цены услуги. Для устойчивой экономики рекомендуется CPL ≤ ${FMT(Math.floor(servicePrice * conv * 0.4))} ₸.`;
  } else {
    msg = `✅ <strong>Экономика сходится.</strong> ROAS ${roas.toFixed(2)}x означает: каждый вложенный рекламный тенге возвращает ${roas.toFixed(2)} ₸ выручки. Ключ к росту — масштабирование бюджета и работа с апсейлом.`;
  }
  document.getElementById('alertBox').innerHTML = msg;
}

// Init
update();
</script>
</body>
</html>
