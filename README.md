<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Catálogo Oficial - Kalil & Doce Tentação</title>
<style>
* {
box-sizing: border-box;
margin: 0;
padding: 0;
font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
body {
background-color: #0b0b0e;
color: #333;
padding: 15px;
display: flex;
flex-direction: column;
align-items: center;
}

/* Topo do Cliente */
.topo-publico {
width: 100%;
max-width: 950px;
display: flex;
justify-content: space-between;
align-items: center;
background: linear-gradient(135deg, #181820, #252532);
padding: 12px 20px;
border-radius: 10px;
margin-bottom: 20px;
border: 1px solid #333;
box-shadow: 0 4px 15px rgba(0,0,0,0.5);
}
.topo-publico h1 {
font-size: 18px;
background: linear-gradient(45deg, #e91e63, #ff4081);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
font-weight: bold;
}
.btn-admin-login {
background-color: #222;
color: #ccc;
border: 1px solid #555;
padding: 6px 14px;
font-size: 11px;
border-radius: 6px;
cursor: pointer;
transition: 0.2s;
}
.btn-admin-login:hover { background-color: #444; color: #fff; }

.catalogo-publico-container {
width: 100%;
max-width: 950px;
}

/* Tela de Seleção Inicial do Cliente */
#tela-selecao-loja {
text-align: center;
padding: 40px 20px;
background: #16161a;
border-radius: 16px;
border: 1px solid #333;
box-shadow: 0 8px 25px rgba(0,0,0,0.5);
margin-top: 20px;
}
#tela-selecao-loja h2 { color: #fff; font-size: 24px; margin-bottom: 10px; }
#tela-selecao-loja p { color: #aaa; font-size: 14px; margin-bottom: 30px; }
.botoes-escolha-loja {
display: flex;
justify-content: center;
gap: 20px;
flex-wrap: wrap;
}
.card-escolha-loja {
background: #22222c;
border: 2px solid #444;
border-radius: 12px;
padding: 25px;
width: 280px;
cursor: pointer;
transition: 0.2s;
text-align: center;
}
.card-escolha-loja:hover {
transform: translateY(-5px);
border-color: #e91e63;
box-shadow: 0 8px 20px rgba(233,30,99,0.3);
}
.card-escolha-loja h3 { font-size: 18px; color: #fff; margin-bottom: 8px; }
.card-escolha-loja p { font-size: 12px; color: #ccc; margin-bottom: 15px; }
.btn-entrar-loja {
background: #e91e63;
color: #fff;
border: none;
padding: 8px 16px;
border-radius: 6px;
font-weight: bold;
font-size: 12px;
cursor: pointer;
}
.btn-entrar-kalil { background: #2e7d32; }

/* Botão Flutuante do Carrinho */
.flutuante-carrinho {
position: fixed;
bottom: 20px;
right: 20px;
background: #25d366;
color: white;
padding: 12px 20px;
border-radius: 30px;
font-weight: bold;
font-size: 14px;
box-shadow: 0 4px 15px rgba(0,0,0,0.4);
cursor: pointer;
z-index: 999;
display: none;
align-items: center;
gap: 8px;
}

/* Modal do Carrinho de Compras */
#modal-carrinho {
position: fixed;
top: 0; left: 0; width: 100%; height: 100%;
background: rgba(0,0,0,0.8);
display: none;
justify-content: center;
align-items: center;
z-index: 9999;
}
.carrinho-box {
background: #1e1e24;
color: #fff;
width: 90%;
max-width: 450px;
padding: 25px;
border-radius: 12px;
box-shadow: 0 5px 25px rgba(0,0,0,0.6);
border: 1px solid #444;
max-height: 90vh;
overflow-y: auto;
}
.carrinho-box h3 { color: #4caf50; font-size: 18px; margin-bottom: 15px; border-bottom: 1px solid #333; padding-bottom: 8px; }
.item-carrinho-lista {
display: flex;
justify-content: space-between;
align-items: center;
background: #262630;
padding: 8px 12px;
border-radius: 6px;
margin-bottom: 8px;
font-size: 12px;
}

/* --- SEÇÃO KALIL (LIMPEZA) --- */
.secao-kalil-encarte {
background: #ffffff;
border-radius: 16px;
overflow: hidden;
margin-bottom: 30px;
box-shadow: 0 8px 25px rgba(0,150,136,0.25);
border: 3px solid #2e7d32;
display: none;
}
.header-kalil {
background: linear-gradient(135deg, rgba(232, 245, 233, 0.95), rgba(200, 230, 201, 0.95)), 
            url('https://images.unsplash.com/photo-1584820927498-cfe5211fd8bf?auto=format&fit=crop&w=1200&q=80');
background-size: cover;
background-position: center;
padding: 25px 20px;
border-bottom: 4px solid #2e7d32;
}
.header-kalil-grid { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 15px; }
.brand-kalil-title { font-size: 38px; font-weight: 900; color: #b71c1c; font-style: italic; line-height: 0.9; }
.brand-kalil-sub { font-size: 14px; color: #2e7d32; font-weight: bold; display: block; margin-top: 4px; }
.slogan-kalil { font-size: 18px; color: #01579b; font-weight: bold; font-style: italic; max-width: 320px; }
.grid-produtos-kalil { display: grid; grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)); gap: 15px; padding: 20px; background: #f4fbf7; }

.card-prod-kalil {
background: #ffffff;
border: 1px solid #c8e6c9;
border-radius: 12px;
padding: 12px;
text-align: center;
box-shadow: 0 4px 10px rgba(0,0,0,0.06);
display: flex;
flex-direction: column;
justify-content: space-between;
}
.card-prod-kalil img { width: 100%; height: 130px; object-fit: contain; margin-bottom: 8px; }
.nome-prod-kalil { font-size: 12px; font-weight: bold; color: #2e7d32; height: 32px; overflow: hidden; margin-bottom: 6px; }
.preco-badge-kalil { background: #0288d1; color: #fff; font-weight: 800; font-size: 14px; padding: 5px 10px; border-radius: 20px; display: inline-block; margin-bottom: 8px; }

/* --- SEÇÃO DOCE TENTAÇÃO (SEXY SHOP & MODA ÍNTIMA) --- */
.secao-doce-encarte {
background: #0a0307;
border-radius: 16px;
overflow: hidden;
margin-bottom: 30px;
box-shadow: 0 8px 25px rgba(233,30,99,0.35);
border: 3px solid #e91e63;
display: none;
}
.header-doce {
background: linear-gradient(135deg, rgba(43, 3, 20, 0.92), rgba(82, 6, 39, 0.92)), 
            url('https://images.unsplash.com/photo-1518199266791-5375a83190b7?auto=format&fit=crop&w=1200&q=80');
background-size: cover;
background-position: center;
padding: 25px 20px;
border-bottom: 4px solid #e91e63;
color: #fff;
}
.header-doce-grid { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 15px; }
.brand-doce-title { font-size: 36px; font-weight: 900; color: #ff4081; font-style: italic; font-family: 'Georgia', serif; line-height: 0.9; }
.brand-doce-sub { font-size: 11px; color: #f8bbd0; letter-spacing: 2px; text-transform: uppercase; display: block; margin-top: 5px; }
.slogan-doce { font-size: 18px; color: #ff80ab; font-weight: bold; font-style: italic; max-width: 320px; }

.subtitulo-categoria-doce { background: linear-gradient(90deg, #ad1457, #e91e63); color: #fff; font-weight: 800; font-size: 13px; padding: 6px 15px; margin: 15px 20px 0 20px; border-radius: 6px; text-transform: uppercase; display: inline-block; }
.grid-produtos-doce { display: grid; grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)); gap: 15px; padding: 15px 20px 20px 20px; }

.card-prod-doce {
background: #ffffff;
border: 2px solid #ff4081;
border-radius: 12px;
padding: 12px;
text-align: center;
box-shadow: 0 4px 12px rgba(0,0,0,0.3);
display: flex;
flex-direction: column;
justify-content: space-between;
}
.card-prod-doce img { width: 100%; height: 130px; object-fit: contain; margin-bottom: 8px; }
.nome-prod-doce { font-size: 12px; font-weight: bold; color: #880e4f; height: 32px; overflow: hidden; margin-bottom: 6px; }
.preco-badge-doce { background: #c2185b; color: #fff; font-weight: 800; font-size: 14px; padding: 5px 10px; border-radius: 20px; display: inline-block; margin-bottom: 8px; }

/* BOTÕES DE AÇÃO */
.btn-add-carrinho {
background: linear-gradient(135deg, #25d366, #128c7e);
color: #fff;
font-weight: bold;
font-size: 11px;
border: none;
padding: 8px;
border-radius: 6px;
cursor: pointer;
width: 100%;
transition: 0.2s;
}
.btn-add-carrinho:hover { opacity: 0.9; }
.btn-voltar-menu {
background: #444; color: #fff; border: none; padding: 8px 15px; border-radius: 6px; font-size: 12px; cursor: pointer; margin-bottom: 15px;
}

/* RODAPÉ DO ENCARTE */
.rodape-encarte {
background: linear-gradient(135deg, #15151c, #0a0a0e); border: 1px solid #333; border-radius: 12px; padding: 15px 20px; color: #aaa; font-size: 11px; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px; margin-top: 30px;
}
.rodape-encarte strong { color: #fff; }

/* ABAS ADMIN E PAINEL */
.nav-tabs { width: 100%; max-width: 950px; display: none; gap: 5px; margin-bottom: 15px; flex-wrap: wrap; }
.tab-btn { flex: 1; min-width: 100px; padding: 10px; background-color: #2c2c35; border: none; font-size: 11px; font-weight: bold; cursor: pointer; border-radius: 6px 6px 0 0; color: #fff; }
.tab-btn.active { background-color: #2e7d32; color: white; }

.view-section { display: none; width: 100%; max-width: 950px; }
.view-section.active { display: block; }

.panel-box { background: #16161a; color: #fff; padding: 20px; border-radius: 12px; box-shadow: 0 0 20px rgba(0,0,0,0.6); margin-bottom: 20px; border: 1px solid #2a2a30; }
.panel-box h2 { color: #4caf50; font-size: 16px; margin-bottom: 12px; border-bottom: 2px solid #2e7d32; padding-bottom: 5px; }
.form-group-inline { display: flex; gap: 8px; margin-bottom: 12px; flex-wrap: wrap; align-items: center; }
.form-group-inline input, .form-group-inline select { flex: 1; min-width: 110px; padding: 8px; border: 1px solid #444; border-radius: 6px; font-size: 12px; background: #222; color: #fff; }
.search-box-container { background: #1e1e24; padding: 10px; border-radius: 8px; border: 1px solid #333; margin-bottom: 15px; display: flex; gap: 8px; align-items: center; }
.search-box-container input { flex: 1; padding: 8px; border: 1px solid #4caf50; border-radius: 6px; font-size: 12px; background: #16161a; color: #fff; }
.btn-action { background-color: #2e7d32; color: white; border: none; padding: 8px 15px; font-weight: bold; border-radius: 6px; cursor: pointer; font-size: 12px; }
.btn-edit { background-color: #0288d1; color: white; border: none; padding: 4px 8px; border-radius: 4px; cursor: pointer; font-size: 10px; }
.btn-delete { background-color: #d32f2f; color: white; border: none; padding: 4px 8px; border-radius: 4px; cursor: pointer; font-size: 10px; }

/* Filtros por Loja no Admin */
.filtros-admin-loja {
display: flex;
gap: 10px;
margin-bottom: 15px;
}
.btn-filtro-admin {
flex: 1;
padding: 8px;
border: 1px solid #444;
background: #222;
color: #aaa;
border-radius: 6px;
cursor: pointer;
font-weight: bold;
font-size: 12px;
}
.btn-filtro-admin.active {
background: #2e7d32;
color: #fff;
border-color: #4caf50;
}

table.stock-table { width: 100%; border-collapse: collapse; margin-top: 10px; }
table.stock-table th { background: #2e7d32; color: white; font-size: 11px; padding: 6px; border: 1px solid #333; }
table.stock-table td { border: 1px solid #333; padding: 6px; font-size: 11px; text-align: center; vertical-align: middle; background: #18181c; color: #fff; }
.produto-img-mini { width: 40px; height: 40px; object-fit: cover; border-radius: 6px; border: 1px solid #444; }
</style>
<script>
let produtosEstoque = JSON.parse(localStorage.getItem('kalil_estoque')) || [
{ cod: "001", nome: "Sabão Líquido 5L", preco: 13.00, qtd: 50, categoria: "Kalil (Limpeza)", imagem: "" },
{ cod: "002", nome: "Desinfetante 2L / 5L", preco: 6.50, qtd: 30, categoria: "Kalil (Limpeza)", imagem: "" },
{ cod: "101", nome: "Conjunto Lingerie Renda Premium", preco: 25.00, qtd: 10, categoria: "Moda Intima Doce Tentação", imagem: "" },
{ cod: "201", nome: "Lubrificante Beijável Love Lub", preco: 17.00, qtd: 20, categoria: "Sexy Shop", imagem: "" }
];

let carrinho = [];
let filtroAdminAtual = 'todos';

function abrirTelaLogin() {
let senhaDigitada = prompt("Digite a senha de Administrador:");
if(senhaDigitada === "Kalil@123") {
document.getElementById('topo-cliente-div').style.display = 'none';
document.getElementById('catalogo-publico-view').style.display = 'none';
document.getElementById('nav-tabs-admin').style.display = 'flex';
document.getElementById('flutuante-carrinho').style.display = 'none';
mudarAba('sec-controle');
} else if(senhaDigitada !== null) {
alert("Senha incorreta!");
}
}

function voltarParaCliente() {
document.getElementById('topo-cliente-div').style.display = 'flex';
document.getElementById('catalogo-publico-view').style.display = 'block';
document.getElementById('nav-tabs-admin').style.display = 'none';
document.querySelectorAll('.view-section').forEach(el => el.classList.remove('active'));
mostrarTelaSelecao();
}

function mostrarTelaSelecao() {
document.getElementById('tela-selecao-loja').style.display = 'block';
document.getElementById('secao-kalil').style.display = 'none';
document.getElementById('secao-doce').style.display = 'none';
document.getElementById('flutuante-carrinho').style.display = 'none';
}

function escolherLoja(tipo) {
document.getElementById('tela-selecao-loja').style.display = 'none';
if(tipo === 'kalil') {
document.getElementById('secao-kalil').style.display = 'block';
document.getElementById('secao-doce').style.display = 'none';
} else {
document.getElementById('secao-kalil').style.display = 'none';
document.getElementById('secao-doce').style.display = 'block';
}
if(carrinho.length > 0) {
document.getElementById('flutuante-carrinho').style.display = 'flex';
}
atualizarCatalogoPublico();
}

function salvarDados() {
localStorage.setItem('kalil_estoque', JSON.stringify(produtosEstoque));
}

function mudarAba(abaId) {
document.querySelectorAll('.view-section').forEach(el => el.classList.remove('active'));
document.querySelectorAll('.tab-btn').forEach(el => el.classList.remove('active'));
document.getElementById(abaId).classList.add('active');
if(abaId === 'sec-controle') {
document.getElementById('btn-aba-estoque').classList.add('active');
atualizarTabelaEstoque();
}
}

function capturarImagemProduto(event) {
let file = event.target.files[0];
if(file) {
let reader = new FileReader();
reader.onload = function(e) {
imagemTempBase64 = e.target.result;
let preview = document.getElementById('preview-prod-img');
preview.src = imagemTempBase64;
preview.style.display = 'inline-block';
};
reader.readAsDataURL(file);
}
}
let imagemTempBase64 = "";

function cadastrarProduto(event) {
event.preventDefault();
let cod = document.getElementById('cad-cod').value.trim();
let nome = document.getElementById('cad-nome').value.trim();
let preco = parseFloat(document.getElementById('cad-preco').value) || 0;
let qtd = parseInt(document.getElementById('cad-qtd').value) || 0;
let categoria = document.getElementById('cad-categoria').value;

if(!cod || !nome) { alert("Preencha Código e Nome!"); return; }

let existente = produtosEstoque.find(p => p.cod === cod);
if(existente) {
existente.nome = nome; existente.preco = preco; existente.qtd = qtd; existente.categoria = categoria;
if(imagemTempBase64) existente.imagem = imagemTempBase64;
} else {
produtosEstoque.push({ cod, nome, preco, qtd, categoria, imagem: imagemTempBase64 || "" });
}

salvarDados();
document.getElementById('form-produto').reset();
document.getElementById('cad-cod').removeAttribute('readonly');
document.getElementById('preview-prod-img').style.display = 'none';
imagemTempBase64 = "";
atualizarTabelaEstoque();
alert("Produto salvo com sucesso!");
}

function editarProduto(cod) {
let p = produtosEstoque.find(item => item.cod === cod);
if(p) {
document.getElementById('cad-cod').value = p.cod;
document.getElementById('cad-cod').setAttribute('readonly', true);
document.getElementById('cad-nome').value = p.nome;
document.getElementById('cad-preco').value = p.preco;
document.getElementById('cad-qtd').value = p.qtd;
document.getElementById('cad-categoria').value = p.categoria || "Kalil (Limpeza)";
imagemTempBase64 = p.imagem || "";

let preview = document.getElementById('preview-prod-img');
if(imagemTempBase64) { preview.src = imagemTempBase64; preview.style.display = 'inline-block'; }
else { preview.style.display = 'none'; }
window.scrollTo({top: 0, behavior: 'smooth'});
}
}

function excluirProduto(cod) {
if(confirm("Deseja excluir este produto do estoque?")) {
produtosEstoque = produtosEstoque.filter(item => item.cod !== cod);
salvarDados();
atualizarTabelaEstoque();
}
}

function filtrarAdmin(tipo) {
filtroAdminAtual = tipo;
document.querySelectorAll('.btn-filtro-admin').forEach(btn => btn.classList.remove('active'));
if(tipo === 'todos') document.getElementById('btn-fil-todos').classList.add('active');
else if(tipo === 'kalil') document.getElementById('btn-fil-kalil').classList.add('active');
else document.getElementById('btn-fil-doce').classList.add('active');
atualizarTabelaEstoque();
}

function atualizarTabelaEstoque() {
let tbody = document.getElementById('tabela-estoque-corpo');
let termo = document.getElementById('busca-estoque-input') ? document.getElementById('busca-estoque-input').value.toLowerCase().trim() : '';
tbody.innerHTML = '';

let filtrados = produtosEstoque.filter(p => {
let matchTermo = p.cod.toLowerCase().includes(termo) || p.nome.toLowerCase().includes(termo);
let cat = p.categoria || "Kalil (Limpeza)";
let matchFiltro = true;
if(filtroAdminAtual === 'kalil') matchFiltro = (cat === "Kalil (Limpeza)");
else if(filtroAdminAtual === 'doce') matchFiltro = (cat !== "Kalil (Limpeza)");
return matchTermo && matchFiltro;
});

filtrados.forEach(p => {
let imgHtml = p.imagem ? `<img src="${p.imagem}" class="produto-img-mini" alt="Foto">` : `<span style="color:#888; font-size:10px;">Sem foto</span>`;
tbody.innerHTML += `
<tr>
<td>${imgHtml}</td>
<td><strong>${p.cod}</strong></td>
<td style="text-align:left;">${p.nome}</td>
<td><span style="background:#222; padding:2px 6px; border-radius:4px; font-size:10px; color:#4caf50; font-weight:bold;">${p.categoria || 'Kalil (Limpeza)'}</span></td>
<td>R$ ${p.preco.toFixed(2).replace('.', ',')}</td>
<td>${p.qtd} un.</td>
<td>
<button class="btn-edit" onclick="editarProduto('${p.cod}')">✏️ Editar</button>
<button class="btn-delete" onclick="excluirProduto('${p.cod}')">🗑️ Excluir</button>
</td>
</tr>
`;
});
}

function adicionarAoCarrinho(cod, nome, preco) {
let itemExistente = carrinho.find(i => i.cod === cod);
if(itemExistente) {
itemExistente.qtd += 1;
} else {
carrinho.push({ cod, nome, preco, qtd: 1 });
}
atualizarCarrinhoBadge();
alert(`"${nome}" foi adicionado ao carrinho!`);
}

function atualizarCarrinhoBadge() {
let totalItens = carrinho.reduce((acc, item) => acc + item.qtd, 0);
document.getElementById('contador-carrinho').innerText = totalItens;
if(totalItens > 0) {
document.getElementById('flutuante-carrinho').style.display = 'flex';
} else {
document.getElementById('flutuante-carrinho').style.display = 'none';
}
}

function abrirCarrinho() {
let listaDiv = document.getElementById('lista-itens-carrinho');
let totalGeralEl = document.getElementById('carrinho-total-geral');
listaDiv.innerHTML = '';

if(carrinho.length === 0) {
listaDiv.innerHTML = `<p style="color:#888; text-align:center; padding:15px;">Seu carrinho está vazio.</p>`;
totalGeralEl.innerText = "R$ 0,00";
} else {
let totalGeral = 0;
carrinho.forEach((item, index) => {
let subtotal = item.preco * item.qtd;
totalGeral += subtotal;
listaDiv.innerHTML += `
<div class="item-carrinho-lista">
<div>
<strong>${item.nome}</strong><br>
<span>R$ ${item.preco.toFixed(2).replace('.', ',')} x ${item.qtd}</span>
</div>
<div style="display:flex; align-items:center; gap:8px;">
<strong>R$ ${subtotal.toFixed(2).replace('.', ',')}</strong>
<button class="btn-delete" onclick="removerItemCarrinho(${index})">X</button>
</div>
</div>
`;
});
totalGeralEl.innerText = "R$ " + totalGeral.toFixed(2).replace('.', ',');
}
document.getElementById('modal-carrinho').style.display = 'flex';
}

function fecharCarrinho() {
document.getElementById('modal-carrinho').style.display = 'none';
}

function removerItemCarrinho(index) {
carrinho.splice(index, 1);
atualizarCarrinhoBadge();
abrirCarrinho();
}

function finalizarPedidoWhatsApp() {
let nomeCliente = document.getElementById('cliente-pedido-nome').value.trim();
if(!nomeCliente) { alert("Por favor, digite o seu nome para enviar o pedido!"); return; }

let totalGeral = 0;
let textoItens = carrinho.map(item => {
let sub = item.preco * item.qtd;
totalGeral += sub;
return `▪️ ${item.qtd}x *${item.nome}* (R$ ${sub.toFixed(2).replace('.', ',')})`;
}).join('\n');

let mensagem = `*Olá! Gostaria de fazer o seguinte pedido:*\n\n` +
`👤 *Cliente:* ${nomeCliente}\n\n` +
`🛍️ *Itens Escolhidos:*\n${textoItens}\n\n` +
`💰 *Valor Total do Pedido:* *R$ ${totalGeral.toFixed(2).replace('.', ',')}*`;

let url = `https://wa.me/5587998071409?text=${encodeURIComponent(mensagem)}`;
window.open(url, '_blank');
}

function atualizarCatalogoPublico() {
let containerKalil = document.getElementById('grid-produtos-kalil');
let containerModa = document.getElementById('grid-produtos-moda');
let containerSexy = document.getElementById('grid-produtos-sexy');

containerKalil.innerHTML = '';
containerModa.innerHTML = '';
containerSexy.innerHTML = '';

produtosEstoque.forEach(p => {
let cat = p.categoria || "Kalil (Limpeza)";
let catImgHtml = p.imagem ? `<img src="${p.imagem}" alt="${p.nome}">` : `<div style="height:130px; background:#f0f0f0; display:flex; align-items:center; justify-content:center; color:#999; font-size:11px; border-radius:8px; margin-bottom:8px;">Foto do Produto</div>`;

let htmlCard = `
<div class="${cat === 'Kalil (Limpeza)' ? 'card-prod-kalil' : 'card-prod-doce'}">
<div>
${catImgHtml}
<div class="${cat === 'Kalil (Limpeza)' ? 'nome-prod-kalil' : 'nome-prod-doce'}">${p.nome}</div>
</div>
<div>
<div class="${cat === 'Kalil (Limpeza)' ? 'preco-badge-kalil' : 'preco-badge-doce'}">R$ ${p.preco.toFixed(2).replace('.', ',')}</div>
<button class="btn-add-carrinho" onclick="adicionarAoCarrinho('${p.cod}', '${p.nome}', ${p.preco})">🛒 Adicionar</button>
</div>
</div>
`;

if(cat === "Kalil (Limpeza)") containerKalil.innerHTML += htmlCard;
else if(cat === "Moda Intima Doce Tentação") containerModa.innerHTML += htmlCard;
else if(cat === "Sexy Shop") containerSexy.innerHTML += htmlCard;
});
}

window.onload = function() {
atualizarCatalogoPublico();
}
</script>
</head>
<body>

<!-- TOPO PÚBLICO -->
<div id="topo-cliente-div" class="topo-publico">
<h1>Kalil & Doce Tentação</h1>
<button class="btn-admin-login" onclick="abrirTelaLogin()">🔒 Área Admin</button>
</div>

<!-- CATÁLOGO PÚBLICO -->
<div id="catalogo-publico-view" class="catalogo-publico-container">

  <!-- TELA 1: ESCOLHA DO CATÁLOGO PELO CLIENTE -->
  <div id="tela-selecao-loja">
    <h2>Selecione o Catálogo Desejado</h2>
    <p>Escolha qual loja você deseja visualizar agora:</p>
    <div class="botoes-escolha-loja">
      <div class="card-escolha-loja" onclick="escolherLoja('kalil')">
        <h3>🧼 Kalil Limpeza</h3>
        <p>Produtos de alta qualidade para o cuidado da sua casa e família.</p>
        <button class="btn-entrar-loja btn-entrar-kalil">Ver Catálogo Kalil</button>
      </div>
      <div class="card-escolha-loja" onclick="escolherLoja('doce')">
        <h3>🔥 Doce Tentação</h3>
        <p>Moda íntima sofisticada e produtos de Sexy Shop com total discrição.</p>
        <button class="btn-entrar-loja">Ver Catálogo Doce Tentação</button>
      </div>
    </div>
  </div>

  <!-- TELA 2: LOJA KALIL (LIMPEZA) -->
  <div id="secao-kalil" class="secao-kalil-encarte">
    <button class="btn-voltar-menu" onclick="mostrarTelaSelecao()">⬅️ Voltar e escolher outro catálogo</button>
    <div class="header-kalil">
      <div class="header-kalil-grid">
        <div>
          <div class="brand-kalil-title">Kalil</div>
          <span class="brand-kalil-sub">Produtos de Limpeza</span>
        </div>
        <div class="slogan-kalil">Qualidade, perfume e limpeza para o seu dia a dia! ♡</div>
      </div>
    </div>
    <div id="grid-produtos-kalil" class="grid-produtos-kalil"></div>
    <div class="rodape-encarte">
      <div>📍 Rua Major João Cordeiro, nº 23 - Centro - Tabira-PE</div>
      <div>💬 Pedidos: (87) 99807-1409</div>
    </div>
  </div>

  <!-- TELA 3: LOJA DOCE TENTAÇÃO (MODA ÍNTIMA & SEXY SHOP) -->
  <div id="secao-doce" class="secao-doce-encarte">
    <button class="btn-voltar-menu" onclick="mostrarTelaSelecao()" style="margin: 15px 20px 0 20px;">⬅️ Voltar e escolher outro catálogo</button>
    <div class="header-doce" style="margin-top: 10px;">
      <div class="header-doce-grid">
        <div>
          <div class="brand-doce-title">Doce Tentação</div>
          <span class="brand-doce-sub">Moda Íntima & Sexy Shop</span>
        </div>
        <div class="slogan-doce">Mais prazer para os seus momentos! ♡</div>
      </div>
    </div>

    <div class="subtitulo-categoria-doce">👙 Moda Íntima</div>
    <div id="grid-produtos-moda" class="grid-produtos-doce"></div>

    <div class="subtitulo-categoria-doce">🔥 Sexy Shop</div>
    <div id="grid-produtos-sexy" class="grid-produtos-doce"></div>

    <div class="rodape-encarte" style="margin: 20px;">
      <div>📍 Rua Major João Cordeiro, nº 23 - Centro - Tabira-PE</div>
      <div>💬 Pedidos: (87) 99807-1409</div>
    </div>
  </div>

</div>

<!-- BOTÃO FLUTUANTE DO CARRINHO -->
<div id="flutuante-carrinho" class="flutuante-carrinho" onclick="abrirCarrinho()">
  🛒 Ver Carrinho (<span id="contador-carrinho">0</span>)
</div>

<!-- MODAL DO CARRINHO DE COMPRAS -->
<div id="modal-carrinho">
  <div class="carrinho-box">
    <h3>🛍️ Seu Carrinho de Compras</h3>
    <div id="lista-itens-carrinho"></div>
    <div style="margin: 15px 0; font-size: 14px; display: flex; justify-content: space-between;">
      <strong>Total do Pedido:</strong>
      <strong id="carrinho-total-geral" style="color: #4caf50;">R$ 0,00</strong>
    </div>
    <div style="margin-bottom: 12px;">
      <label style="font-size: 11px; display: block; margin-bottom: 4px;">Seu Nome:</label>
      <input type="text" id="cliente-pedido-nome" placeholder="Digite seu nome completo" style="width: 100%; padding: 8px; border-radius: 4px; border: 1px solid #444; background: #222; color: #fff; font-size: 12px;">
    </div>
    <div style="display: flex; gap: 8px;">
      <button class="btn-action" style="flex: 1; background: #25d366; padding: 10px;" onclick="finalizarPedidoWhatsApp()">💬 Enviar Pedido no Zap</button>
      <button class="btn-delete" style="padding: 10px;" onclick="fecharCarrinho()">Fechar</button>
    </div>
  </div>
</div>

<!-- ABAS ADMINISTRATIVAS -->
<div id="nav-tabs-admin" class="nav-tabs">
<button id="btn-aba-estoque" class="tab-btn active" onclick="mudarAba('sec-controle')">📦 Estoque & Lojas</button>
<button class="tab-btn" style="background:#b71c1c;" onclick="voltarParaCliente()">👁️ Ver Catálogo do Cliente</button>
</div>

<!-- ABA 1: ESTOQUE (ADMIN) -->
<div id="sec-controle" class="view-section">
<div class="panel-box">
<h2>Cadastrar / Atualizar Produto no Estoque</h2>
<form id="form-produto" onsubmit="cadastrarProduto(event)">
<div class="form-group-inline">
<input type="text" id="cad-cod" placeholder="Código (Ex: 001)" required>
<input type="text" id="cad-nome" placeholder="Nome do Produto" required>
<select id="cad-categoria" required>
<option value="Kalil (Limpeza)">Kalil (Limpeza)</option>
<option value="Moda Intima Doce Tentação">Moda Intima Doce Tentação</option>
<option value="Sexy Shop">Sexy Shop</option>
</select>
</div>
<div class="form-group-inline">
<input type="number" step="0.01" id="cad-preco" placeholder="Preço Unit. (R$)" required>
<input type="number" id="cad-qtd" placeholder="Qtd em Estoque" required>
</div>
<div class="form-group-inline" style="align-items: center; margin-top: 8px;">
<label style="font-size: 11px; font-weight: bold; color: #4caf50;">📷 Foto do Produto:</label>
<input type="file" accept="image/*" onchange="capturarImagemProduto(event)" style="background: #222; padding: 4px;">
<img id="preview-prod-img" style="width: 35px; height: 35px; object-fit: cover; border-radius: 4px; display: none; border: 1px solid #444;" alt="Preview">
<button type="submit" class="btn-action" style="flex: 1; padding: 9px;">Salvar no Estoque</button>
</div>
</form>

<h2 style="margin-top: 25px;">Gerenciar Produtos por Loja</h2>
<div class="filtros-admin-loja">
<button id="btn-fil-todos" class="btn-filtro-admin active" onclick="filtrarAdmin('todos')">🌐 Todos os Produtos</button>
<button id="btn-fil-kalil" class="btn-filtro-admin" onclick="filtrarAdmin('kalil')">🧼 Kalil (Limpeza)</button>
<button id="btn-fil-doce" class="btn-filtro-admin" onclick="filtrarAdmin('doce')">🔥 Doce Tentação & Sexy Shop</button>
</div>

<div class="search-box-container">
<span>🔍</span>
<input type="text" id="busca-estoque-input" placeholder="Pesquisar produto no estoque por código ou nome..." oninput="atualizarTabelaEstoque()">
</div>

<table class="stock-table">
<thead>
<tr>
<th style="width: 8%;">FOTO</th>
<th style="width: 12%;">CÓDIGO</th>
<th style="width: 30%;">PRODUTO</th>
<th style="width: 20%;">CATEGORIA</th>
<th style="width: 12%;">PREÇO</th>
<th style="width: 8%;">QTD</th>
<th style="width: 10%;">AÇÕES</th>
</tr>
</thead>
<tbody id="tabela-estoque-corpo">
</tbody>
</table>
</div>
</div>

</body>
</html>
