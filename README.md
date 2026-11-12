
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#102c35">
<title>Elite Pregão Pro | Inteligência em Licitações</title>
<style>
:root{
 --navy:#102c35;--navy2:#173e49;--green:#19a879;
 --green2:#0e8961;--bg:#f3f6f7;--white:#fff;
 --text:#24353c;--muted:#7b8b91;--border:#e3e9eb;
 --red:#d9534f;--orange:#df963b;--blue:#3b82b8;
}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);font-family:Inter,Arial,sans-serif;color:var(--text)}
button,input,select,textarea{font:inherit}
button{cursor:pointer}
.app{display:flex;min-height:100vh}
.sidebar{width:255px;background:var(--navy);color:white;padding:22px 15px;position:fixed;inset:0 auto 0 0;overflow-y:auto;z-index:10}
.brand{display:flex;align-items:center;gap:11px;padding:5px 8px 25px;border-bottom:1px solid #ffffff20}
.logo{height:42px;width:42px;border-radius:12px;background:var(--green);display:grid;place-items:center;font-weight:900;font-size:21px}
.brand strong{font-size:16px;display:block}
.brand small{color:#a8c1c5;font-size:10px;letter-spacing:1px}
.navlabel{font-size:10px;color:#819ba2;font-weight:bold;letter-spacing:1.5px;padding:23px 10px 8px}
.nav button{width:100%;border:0;background:none;color:#c1d0d3;text-align:left;padding:12px 13px;border-radius:8px;margin:2px 0;font-size:13px;display:flex;gap:12px;align-items:center}
.nav button:hover,.nav button.active{background:#ffffff17;color:white}
.nav button.active{border-left:3px solid #28c48c}
.nav .ico{width:20px;text-align:center;font-size:16px}
.sidebar-foot{border-top:1px solid #ffffff20;margin-top:25px;padding:17px 8px;color:#a8c1c5;font-size:11px}
.main{margin-left:255px;width:calc(100% - 255px)}
.topbar{height:70px;background:white;border-bottom:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;padding:0 30px;position:sticky;top:0;z-index:5}
.top-title{font-weight:700;font-size:14px}
.top-right{display:flex;align-items:center;gap:15px}
.status{font-size:11px;color:var(--green);background:#e7f7f0;padding:8px 12px;border-radius:30px}
.avatar{background:var(--navy);color:white;border-radius:50%;width:35px;height:35px;display:grid;place-items:center;font-size:12px;font-weight:bold}
.content{padding:30px;max-width:1600px;margin:auto}
.pagehead{display:flex;justify-content:space-between;align-items:center;gap:15px;margin-bottom:25px}
h1{font-size:25px;margin:0 0 7px;color:var(--navy)}
.subtitle{color:var(--muted);font-size:13px}
.btn{border:0;background:var(--green);color:white;padding:11px 16px;border-radius:7px;font-size:12px;font-weight:bold}
.btn:hover{background:var(--green2)}
.btn.secondary{background:white;color:var(--navy);border:1px solid var(--border)}
.btn.dark{background:var(--navy)}
.btn.danger{background:var(--red)}
.grid{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:16px;margin-bottom:22px}
.card{background:white;border:1px solid var(--border);border-radius:11px;padding:20px;box-shadow:0 2px 8px #102c3507}
.metric-label{font-size:12px;color:var(--muted);margin-bottom:12px}
.metric{font-size:27px;font-weight:800;color:var(--navy)}
.metric-note{font-size:11px;color:var(--green);margin-top:8px}
.panel{background:white;border:1px solid var(--border);border-radius:11px;padding:21px;margin-bottom:20px}
.panel-title{font-size:15px;font-weight:750;color:var(--navy);margin-bottom:17px}
.two{display:grid;grid-template-columns:1.5fr 1fr;gap:18px}
.tablewrap{overflow-x:auto}
table{width:100%;border-collapse:collapse;min-width:650px}
th{text-align:left;background:#f7f9fa;color:#718188;font-size:10px;text-transform:uppercase;letter-spacing:.6px;padding:13px}
td{padding:14px 13px;border-bottom:1px solid var(--border);font-size:12px}
tr:last-child td{border-bottom:0}
.pill{display:inline-block;padding:5px 9px;border-radius:20px;background:#edf3f4;color:#46616a;font-size:10px;font-weight:bold}
.pill.green{background:#e4f6ed;color:#168458}
.pill.orange{background:#fff2df;color:#b8751b}
.pill.red{background:#ffebeb;color:#bd4545}
.pill.blue{background:#e8f1fc;color:#3976ae}
input,select,textarea{border:1px solid var(--border);border-radius:7px;padding:11px;background:white;color:var(--text);width:100%;font-size:12px;outline:none}
input:focus,select:focus,textarea:focus{border-color:var(--green)}
label{font-size:11px;font-weight:700;color:#63757c;display:block;margin:13px 0 6px}
.formgrid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:12px}
.actions{display:flex;gap:8px;flex-wrap:wrap;margin-top:16px}
.searchbar{display:flex;gap:10px;margin-bottom:15px}
.searchbar input{max-width:350px}
.pipeline{display:grid;grid-template-columns:repeat(4,minmax(170px,1fr));gap:12px;overflow-x:auto}
.stage{background:#f3f6f7;border-radius:9px;padding:12px;min-height:200px}
.stagehead{font-size:11px;font-weight:800;color:var(--navy);margin-bottom:12px;display:flex;justify-content:space-between}
.opcard{background:white;border:1px solid var(--border);padding:13px;border-radius:8px;margin-bottom:9px}
.opcard strong{font-size:12px;display:block;margin-bottom:8px}
.opcard small{color:var(--muted);font-size:10px}
.bar{height:8px;background:#edf1f2;border-radius:10px;overflow:hidden;margin:10px 0}
.bar span{display:block;height:100%;background:var(--green);border-radius:10px}
.empty{padding:30px;text-align:center;color:var(--muted);font-size:12px}
.notice{padding:13px;background:#edf7f4;border-left:3px solid var(--green);font-size:12px;border-radius:5px;margin-bottom:15px}
.result{font-size:22px;font-weight:800;color:var(--green);margin-top:12px}
.mobilemenu{display:none;border:0;background:none;font-size:22px}
.modalbg{position:fixed;inset:0;background:#0008;display:none;align-items:center;justify-content:center;z-index:30;padding:15px}
.modal{background:white;border-radius:12px;padding:25px;width:min(500px,100%);max-height:90vh;overflow:auto}
.modal h2{font-size:18px;color:var(--navy);margin-top:0}
.toast{position:fixed;bottom:20px;right:20px;background:var(--navy);color:white;padding:14px 20px;border-radius:8px;display:none;z-index:50;font-size:12px}
.footer{text-align:center;color:#9aa7aa;font-size:10px;padding:20px}
@media(max-width:950px){
 .sidebar{transform:translateX(-100%);transition:.2s}
 .sidebar.open{transform:translateX(0)}
 .main{margin-left:0;width:100%}
 .mobilemenu{display:block}
 .grid{grid-template-columns:repeat(2,minmax(0,1fr))}
 .two{grid-template-columns:1fr}
 .content{padding:20px 14px}
 .topbar{padding:0 15px}
}
@media(max-width:550px){
 .grid{grid-template-columns:1fr 1fr;gap:9px}
 .card{padding:14px}
 .metric{font-size:21px}
 .pagehead{align-items:flex-start;flex-direction:column}
 .formgrid{grid-template-columns:1fr}
}
</style>
</head>
<body>
<div class="app">
<aside class="sidebar" id="sidebar">
 <div class="brand">
  <div class="logo">EP</div>
  <div><strong>ELITE PREGÃO PRO</strong><small>INTELIGÊNCIA EM LICITAÇÕES</small></div>
 </div>
 <div class="nav">
  <div class="navlabel">PRINCIPAL</div>
  <button class="active" data-page="dashboard"><span class="ico">▦</span>Visão geral</button>
  <button data-page="oportunidades"><span class="ico">⌕</span>Oportunidades</button>
  <button data-page="funil"><span class="ico">◫</span>Funil de licitações</button>
  <button data-page="agenda"><span class="ico">▣</span>Agenda</button>
  <div class="navlabel">INTELIGÊNCIA</div>
  <button data-page="mercado"><span class="ico">◈</span>Mercado e preços</button>
  <button data-page="precificacao"><span class="ico">▤</span>Precificação</button>
  <button data-page="analise"><span class="ico">✧</span>Análise de edital</button>
  <div class="navlabel">OPERAÇÃO</div>
  <button data-page="documentos"><span class="ico">▧</span>Documentos</button>
  <button data-page="pregao"><span class="ico">⚖</span>Sala de pregão</button>
  <button data-page="antecipa"><span class="ico">↗</span>AntecipaGov</button>
  <div class="navlabel">ADMINISTRAÇÃO</div>
  <button data-page="empresa"><span class="ico">▣</span>Minha empresa</button>
 </div>
 <div class="sidebar-foot">ELITE PREGÃO PRO<br>Versão demonstrativa 1.0</div>
</aside>
<main class="main">
<header class="topbar">
 <div style="display:flex;align-items:center;gap:12px">
  <button class="mobilemenu" onclick="document.getElementById('sidebar').classList.toggle('open')">☰</button>
  <div class="top-title">CENTRAL DE INTELIGÊNCIA</div>
 </div>
 <div class="top-right"><span class="status">● Sistema local ativo</span><div class="avatar">EP</div></div>
</header>
<div class="content" id="content"></div>
<div class="footer">ELITE PREGÃO PRO · Plataforma de inteligência e gestão de licitações públicas</div>
</main>
</div>
<div class="modalbg" id="modalbg">
 <div class="modal" id="modal"></div>
</div>
<div class="toast" id="toast"></div>
<script>
const $=s=>document.querySelector(s);
const money=v=>Number(v||0).toLocaleString('pt-BR',{style:'currency',currency:'BRL'});
const today=()=>new Date().toISOString().slice(0,10);
const load=(k,d)=>{try{return JSON.parse(localStorage.getItem('ep_'+k))??d}catch{return d}};
const save=(k,v)=>localStorage.setItem('ep_'+k,JSON.stringify(v));
let opportunities=load('opportunities',[
{id:1,title:'Aquisição de materiais de escritório',agency:'Prefeitura Municipal',number:'PE 012/2026',value:45000,stage:'Oportunidade',date:'2026-12-10',status:'Em análise'},
{id:2,title:'Fornecimento de equipamentos de informática',agency:'Secretaria de Educação',number:'PE 025/2026',value:120000,stage:'Análise do edital',date:'2026-12-15',status:'Em análise'},
{id:3,title:'Materiais de limpeza',agency:'Hospital Municipal',number:'PE 031/2026',value:28000,stage:'Documentação',date:'2026-12-18',status:'Em andamento'}
]);
let tasks=load('tasks',[]);
let docs=load('docs',[]);
let company=load('company',{name:'Minha empresa',cnpj:'',email:'',phone:'',address:''});
let page='dashboard';
const stages=['Oportunidade','Análise do edital','Documentação','Proposta','Disputa','Habilitação','Ganho','Perdido'];
function persist(){save('opportunities',opportunities);save('tasks',tasks);save('docs',docs);save('company',company)}
function toast(msg){let t=$('#toast');t.textContent=msg;t.style.display='block';setTimeout(()=>t.style.display='none',2600)}
function heading(title,sub,button=''){return `<div class="pagehead"><div><h1>${title}</h1><div class="subtitle">${sub}</div></div>${button}</div>`}
function metric(label,value,note){return `<div class="card"><div class="metric-label">${label}</div><div class="metric">${value}</div><div class="metric-note">${note}</div></div>`}
function go(p){
 page=p;document.querySelectorAll('.nav button').forEach(b=>b.classList.toggle('active',b.dataset.page===p));
 $('#sidebar').classList.remove('open');render()
}
document.querySelectorAll('.nav button').forEach(b=>b.onclick=()=>go(b.dataset.page));
function render(){
 const c=$('#content');
 const total=opportunities.reduce((a,o)=>a+Number(o.value||0),0);
 const active=opportunities.filter(o=>!['Ganho','Perdido'].includes(o.stage));
 if(page==='dashboard'){
 c.innerHTML=heading('Visão geral','Acompanhe os indicadores e a operação da sua empresa.')+
 `<div class="grid">${metric('Oportunidades cadastradas',opportunities.length,'Licitações no seu controle')}${metric('Valor potencial',money(total),'Soma dos valores cadastrados')}${metric('Em andamento',active.length,'Oportunidades não encerradas')}${metric('Tarefas pendentes',tasks.filter(t=>!t.done).length,'Atividades a realizar')}</div>
 <div class="two"><div class="panel"><div class="panel-title">Oportunidades recentes</div>${tableOpp(opportunities.slice(0,5))}</div><div class="panel"><div class="panel-title">Distribuição do funil</div>${stages.map(s=>{let n=opportunities.filter(o=>o.stage===s).length;return `<div style="font-size:11px;margin:12px 0">${s}<b style="float:right">${n}</b></div><div class="bar"><span style="width:${opportunities.length?n/opportunities.length*100:0}%"></span></div>`}).join('')}</div></div>
 <div class="panel"><div class="panel-title">Próximas atividades</div>${taskList(tasks.filter(t=>!t.done).slice(0,5))}</div>`;
 }
 if(page==='oportunidades'){
 c.innerHTML=heading('Oportunidades','Gerencie licitações identificadas e acompanhe seus prazos.',`<button class="btn" onclick="newOpp()">+ Nova oportunidade</button>`)+
 `<div class="panel"><div class="searchbar"><input id="searchOpp" placeholder="Pesquisar objeto, órgão ou número..." oninput="filterOpp()"><select id="stageFilter" onchange="filterOpp()" style="max-width:220px"><option value="">Todas as etapas</option>${stages.map(s=>`<option>${s}</option>`).join('')}</select></div><div id="oppTable">${tableOpp(opportunities)}</div></div>`;
 }
 if(page==='funil'){
 c.innerHTML=heading('Funil de licitações','Acompanhe cada oportunidade desde a descoberta até o encerramento.')+
 `<div class="pipeline">${stages.map(s=>{let list=opportunities.filter(o=>o.stage===s);return `<div class="stage"><div class="stagehead">${s}<span>${list.length}</span></div>${list.map(o=>`<div class="opcard"><strong>${esc(o.title)}</strong><small>${esc(o.number)} · ${money(o.value)}</small><div style="margin-top:10px"><select onchange="moveOpp(${o.id},this.value)">${stages.map(x=>`<option ${x===s?'selected':''}>${x}</option>`).join('')}</select></div></div>`).join('')}</div>`}).join('')}</div>`;
 }
 if(page==='agenda'){
 c.innerHTML=heading('Agenda','Prazos, tarefas e compromissos da operação.',`<button class="btn" onclick="newTask()">+ Nova tarefa</button>`)+
 `<div class="panel"><div class="panel-title">Todas as atividades</div>${taskList(tasks)}</div>`;
 }
 if(page==='mercado'){
 c.innerHTML=heading('Mercado e inteligência de preços','Área de referência para pesquisas de mercado.')+
 `<div class="notice">Os dados abaixo são apenas demonstrativos. Para decisões de preço, consulte fontes oficiais e registros verificáveis.</div><div class="grid">${metric('Fontes previstas','PNCP','Contratações públicas')}${metric('Catálogo','CATMAT','Materiais')}${metric('Catálogo','CATSER','Serviços')}${metric('Histórico','Preços','Não equivale a cotação atual')}</div><div class="panel"><div class="panel-title">Pesquisa de mercado</div><label>Termo ou descrição do item</label><input id="marketTerm" placeholder="Ex.: papel A4, computador, serviço de limpeza"><div class="actions"><button class="btn" onclick="toast('Pesquisa externa ainda não conectada. Consulte o PNCP e os catálogos oficiais.')">Pesquisar</button><button class="btn secondary" onclick="window.open('https://pncp.gov.br/','_blank')">Abrir PNCP oficial ↗</button></div></div>`;
 }
 if(page==='precificacao'){
 c.innerHTML=heading('Precificação inteligente','Calcule o preço mínimo de venda considerando custos, encargos e margem.')+
 `<div class="panel"><div class="panel-title">Calculadora de preço mínimo</div><div class="formgrid"><div><label>Custo total (R$)</label><input id="cost" type="number" min="0" step=".01" value="1000"></div><div><label>Encargos sobre a venda (%)</label><input id="fees" type="number" min="0" max="99.99" step=".01" value="10"></div><div><label>Margem desejada sobre a venda (%)</label><input id="margin" type="number" min="0" max="99.99" step=".01" value="20"></div></div><div class="actions"><button class="btn" onclick="calculate()">Calcular preço mínimo</button></div><div id="priceResult"></div><div class="notice" style="margin-top:20px">Fórmula: preço mínimo = custo total ÷ (1 − encargos − margem). Informe percentuais em relação ao preço de venda. O cálculo não substitui análise tributária ou contábil.</div></div>`;
 calculate();
 }
 if(page==='analise'){
 c.innerHTML=heading('Análise de edital','Organize a leitura e a conferência de requisitos do instrumento convocatório.')+
 `<div class="notice">A análise automatizada por IA ainda não está conectada. Use este checklist para registrar a revisão humana do edital.</div><div class="panel"><div class="panel-title">Checklist de análise</div>${['Objeto e especificações','Data e horário da sessão','Critério de julgamento','Modo de disputa','Documentação de habilitação','Qualificação técnica','Exigências econômico-financeiras','Prazos de entrega','Local de entrega','Condições de pagamento','Sanções e penalidades','Impugnação e recursos'].map((x,i)=>`<label style="font-weight:500;font-size:12px"><input type="checkbox" style="width:auto;margin-right:8px"> ${x}</label>`).join('')}<label>Observações da análise</label><textarea rows="4" placeholder="Registre riscos, exigências e pontos de atenção..."></textarea><div class="actions"><button class="btn" onclick="toast('Checklist revisado nesta sessão. Salve suas observações externamente.')">Concluir revisão</button></div></div>`;
 }
 if(page==='documentos'){
 c.innerHTML=heading('Central de documentos','Controle demonstrativo de documentos da empresa.',`<button class="btn" onclick="newDoc()">+ Cadastrar documento</button>`)+
 `<div class="notice">Esta versão armazena metadados localmente. Não envie documentos sigilosos: ainda não existe armazenamento privado com controle de acesso.</div><div class="panel"><div class="panel-title">Documentos cadastrados</div>${docs.length?`<div class="tablewrap"><table><thead><tr><th>Documento</th><th>Categoria</th><th>Validade</th><th>Ações</th></tr></thead><tbody>${docs.map(d=>`<tr><td>${esc(d.name)}</td><td>${esc(d.category)}</td><td>${d.date||'Não informada'}</td><td><button class="btn danger" onclick="deleteDoc(${d.id})">Excluir</button></td></tr>`).join('')}</tbody></table></div>`:'<div class="empty">Nenhum documento cadastrado.</div>'}</div>`;
 }
 if(page==='pregao'){
 c.innerHTML=heading('Sala de pregão','Painel de apoio para acompanhamento manual da sessão.')+
 `<div class="notice">A sala não está conectada a sistemas de disputa. Não envia lances, não acessa credenciais e não executa ações em nome do fornecedor.</div><div class="panel"><div class="panel-title">Controle manual de disputa</div><div class="formgrid"><div><label>Pregão / processo</label><input id="auction" placeholder="Ex.: PE 012/2026"></div><div><label>Item</label><input id="item" placeholder="Número do item"></div><div><label>Seu lance atual (R$)</label><input id="bid" type="number" step=".01"></div><div><label>Limite mínimo calculado (R$)</label><input id="limit" type="number" step=".01"></div></div><div class="actions"><button class="btn" onclick="checkBid()">Verificar lance</button></div><div id="bidResult"></div></div>`;
 }
 if(page==='antecipa'){
 c.innerHTML=heading('AntecipaGov','Informações para planejamento de antecipação de recebíveis.')+
 `<div class="notice">Este módulo é informativo. Não há integração financeira, consulta de crédito ou contratação de antecipação nesta versão.</div><div class="panel"><div class="panel-title">O que considerar</div><ul style="font-size:13px;line-height:2;color:#52656c"><li>Verifique se o contrato e o recebível são elegíveis.</li><li>Consulte as condições da instituição financeira habilitada.</li><li>Compare custo efetivo, taxas e prazo de liquidação.</li><li>Confirme os dados diretamente nos canais oficiais.</li></ul><button class="btn" onclick="window.open('https://www.gov.br/','_blank')">Consultar portal Gov.br ↗</button></div>`;
 }
 if(page==='empresa'){
 c.innerHTML=heading('Minha empresa','Dados cadastrais e informações do fornecedor.')+
 `<div class="panel"><div class="panel-title">Cadastro empresarial</div><div class="formgrid"><div><label>Razão social / Nome</label><input id="coName" value="${attr(company.name)}"></div><div><label>CNPJ</label><input id="coCnpj" value="${attr(company.cnpj)}" placeholder="00.000.000/0000-00"></div><div><label>E-mail</label><input id="coEmail" value="${attr(company.email)}"></div><div><label>Telefone</label><input id="coPhone" value="${attr(company.phone)}"></div></div><label>Endereço</label><input id="coAddress" value="${attr(company.address)}"><div class="actions"><button class="btn" onclick="saveCompany()">Salvar cadastro</button></div></div><div class="panel"><div class="panel-title">Dados e privacidade</div><p style="font-size:12px;color:#718188;line-height:1.7">As informações desta demonstração ficam no armazenamento local deste navegador. Não existe login, sincronização entre dispositivos ou isolamento seguro entre empresas.</p><button class="btn secondary" onclick="exportData()">Exportar meus dados (JSON)</button></div>`;
 }
}
function esc(s){return String(s??'').replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]))}
function attr(s){return esc(s).replace(/`/g,'&#96;')}
function tableOpp(list){
 if(!list.length)return '<div class="empty">Nenhuma oportunidade cadastrada.</div>';
 return `<div class="tablewrap"><table><thead><tr><th>Objeto</th><th>Órgão</th><th>Processo</th><th>Valor estimado</th><th>Etapa</th><th>Prazo</th><th></th></tr></thead><tbody>${list.map(o=>`<tr><td><b>${esc(o.title)}</b></td><td>${esc(o.agency)}</td><td>${esc(o.number)}</td><td>${money(o.value)}</td><td><span class="pill ${o.stage==='Ganho'?'green':o.stage==='Perdido'?'red':'blue'}">${esc(o.stage)}</span></td><td>${o.date||'—'}</td><td><button class="btn secondary" onclick="editOpp(${o.id})">Editar</button></td></tr>`).join('')}</tbody></table></div>`;
}
function filterOpp(){
 let q=$('#searchOpp').value.toLowerCase(),s=$('#stageFilter').value;
 $('#oppTable').innerHTML=tableOpp(opportunities.filter(o=>(o.title+' '+o.agency+' '+o.number).toLowerCase().includes(q)&&(!s||o.stage===s)));
}
function newOpp(o=null){
 const edit=!!o;
 showModal(`<h2>${edit?'Editar':'Nova'} oportunidade</h2><form id="oppForm"><label>Objeto</label><input name="title" required value="${attr(o?.title||'')}"><label>Órgão</label><input name="agency" required value="${attr(o?.agency||'')}"><div class="formgrid"><div><label>Número do processo</label><input name="number" value="${attr(o?.number||'')}"></div><div><label>Valor estimado (R$)</label><input name="value" type="number" step=".01" value="${o?.value||0}"></div><div><label>Prazo / Sessão</label><input name="date" type="date" value="${o?.date||''}"></div><div><label>Etapa</label><select name="stage">${stages.map(s=>`<option ${o?.stage===s?'selected':''}>${s}</option>`).join('')}</select></div></div><div class="actions"><button class="btn">Salvar oportunidade</button><button type="button" class="btn secondary" onclick="closeModal()">Cancelar</button></div></form>`);
 $('#oppForm').onsubmit=e=>{e.preventDefault();let f=new FormData(e.target),v=Object.fromEntries(f);v.id=o?.id||Date.now();v.value=Number(v.value);if(edit)opportunities=opportunities.map(x=>x.id===o.id?v:x);else opportunities.unshift(v);persist();closeModal();render();toast('Oportunidade salva.')};
}
function editOpp(id){let o=opportunities.find(x=>x.id===id);if(o)newOpp(o)}
function moveOpp(id,stage){opportunities=opportunities.map(o=>o.id===id?{...o,stage}:o);persist();render();toast('Etapa atualizada.')}
function newTask(){
 showModal(`<h2>Nova tarefa</h2><form id="taskForm"><label>Descrição</label><input name="title" required><div class="formgrid"><div><label>Responsável</label><input name="owner" placeholder="Nome"></div><div><label>Data</label><input name="date" type="date" value="${today()}"></div></div><label>Observação</label><textarea name="note" rows="3"></textarea><div class="actions"><button class="btn">Salvar tarefa</button><button type="button" class="btn secondary" onclick="closeModal()">Cancelar</button></div></form>`);
 $('#taskForm').onsubmit=e=>{e.preventDefault();let v=Object.fromEntries(new FormData(e.target));tasks.push({...v,id:Date.now(),done:false});persist();closeModal();render();toast('Tarefa criada.')};
}
function taskList(list){
 if(!list.length)return '<div class="empty">Nenhuma atividade cadastrada.</div>';
 return `<div class="tablewrap"><table><thead><tr><th>Atividade</th><th>Responsável</th><th>Data</th><th>Status</th><th>Ação</th></tr></thead><tbody>${list.map(t=>`<tr><td>${esc(t.title)}<br><small style="color:#8b999d">${esc(t.note||'')}</small></td><td>${esc(t.owner||'—')}</td><td>${t.date||'—'}</td><td><span class="pill ${t.done?'green':'orange'}">${t.done?'Concluída':'Pendente'}</span></td><td>${t.done?'':`<button class="btn secondary" onclick="doneTask(${t.id})">Concluir</button>`}</td></tr>`).join('')}</tbody></table></div>`;
}
function doneTask(id){tasks=tasks.map(t=>t.id===id?{...t,done:true}:t);persist();render();toast('Tarefa concluída.')}
function newDoc(){
 showModal(`<h2>Cadastrar documento</h2><form id="docForm"><label>Nome</label><input name="name" required><label>Categoria</label><select name="category"><option>Habilitação jurídica</option><option>Fiscal e trabalhista</option><option>Econômico-financeira</option><option>Qualificação técnica</option><option>Outros</option></select><label>Data de validade</label><input type="date" name="date"><div class="actions"><button class="btn">Cadastrar</button><button type="button" class="btn secondary" onclick="closeModal()">Cancelar</button></div></form>`);
 $('#docForm').onsubmit=e=>{e.preventDefault();docs.push({...Object.fromEntries(new FormData(e.target)),id:Date.now()});persist();closeModal();render();toast('Documento cadastrado.')};
}
function deleteDoc(id){if(confirm('Excluir este cadastro?')){docs=docs.filter(d=>d.id!==id);persist();render()}}
function calculate(){
 let cost=Number($('#cost')?.value||0),fees=Number($('#fees')?.value||0)/100,margin=Number($('#margin')?.value||0)/100;
 let el=$('#priceResult');if(!el)return;
 if(fees+margin>=1||cost<0){el.innerHTML='<div class="result" style="color:var(--red)">Percentuais inválidos. A soma deve ser inferior a 100%.</div>';return}
 let price=cost/(1-fees-margin);
 el.innerHTML=`<div class="result">Preço mínimo: ${money(price)}</div><p style="font-size:12px;color:#718188">Custo: ${money(cost)} · Encargos: ${money(price*fees)} · Margem: ${money(price*margin)}</p>`;
}
function checkBid(){
 let bid=Number($('#bid').value),limit=Number($('#limit').value);
 let el=$('#bidResult');
 if(!bid||!limit){el.innerHTML='<p>Preencha o lance e o limite mínimo.</p>';return}
 el.innerHTML=bid<limit?'<div class="result" style="color:var(--red)">ATENÇÃO: lance abaixo do limite informado.</div>':'<div class="result">Lance dentro do limite informado.</div>';
}
function saveCompany(){
 company={name:$('#coName').value,cnpj:$('#coCnpj').value,email:$('#coEmail').value,phone:$('#coPhone').value,address:$('#coAddress').value};persist();toast('Cadastro salvo.')
}
function exportData(){
 let data={opportunities,tasks,docs,company,exportedAt:new Date().toISOString()};
 let a=document.createElement('a');a.href=URL.createObjectURL(new Blob([JSON.stringify(data,null,2)],{type:'application/json'}));a.download='elite-pregao-pro-dados.json';a.click();URL.revokeObjectURL(a.href);
}
function showModal(html){$('#modal').innerHTML=html;$('#modalbg').style.display='flex'}
function closeModal(){$('#modalbg').style.display='none'}
$('#modalbg').addEventListener('click',e=>{if(e.target.id==='modalbg')closeModal()});
render();
</script>
</body>
</html>
