Configuração de ambientes para automação

MOCHA
1) Instalar o nodejs
2) Instalar o npm
3) Instalar via comando o mocha - npm install mocha --> Obs.: Sempre no diretório aonde o NODEJs foi instalado (no meu caso: C:\Program Files\nodejs)
4) Instalar via comando o instanbul - npm install --save-dev istanbul

Sites de apoio: https://blog.getty.io/cobertura-de-c%C3%B3digo-no-seu-projeto-nodejs-usando-istanbul-f6bac73e4408
http://agiletesters.com.br/topic/623/testes-end2end-em-node-js-webdriverio-gulp-e-mocha


Listagem dos Assert's utilizados:
1) Assert.isfunction
isFunction(valor, [mensagem])
•	@param { Mixed } valor
•	@param { String } mensagem
Confirma que o valor é uma função.
Exemplo:
function serveChá() { 
return 'xícara de chá'; 
};
assert.isFunction(serveChá, 'Temos chá agora');
2)  Assert.intanceOf 
.instanceOf(objeto, construtor, [mensagem])
•	@param { Objeto } objeto
•	@param { Construtor } construtor
•	@param { String } mensagem
Confirma que valor é uma instância de construtor.
var Chá = function (nome)
{ 
this.nome = nome; 
} , 
chai = new Chá('chai'); 
assert.instanceOf(chai, Chá, 'chai é uma instância de chá');
3) Assert.equal
.equal(actual, expected, [message])
•	@param { Mixed } atual
•	@param { Mixed } esperado
•	@param { String } mensagem
Confirma igualdade não rigorosa (==) do atual e esperado.
assert.equal(3, '3', '== transforma valores para string');
4) Assert.property
.property(object, property, [message])
•	@param { Object } object
•	@param { String } property
•	@param { String } message
Confirma que objeto tem uma propriedade direta ou herdada nomeada por property.
assert.property({ chá: { verde: 'matcha' }}, 'chá');
assert.property({ chá: { verde: 'matcha' }}, 'toString');
4) Assert.propertyVal
.propertyVal(object, property, value, [message])
•	@param { Object } object
•	@param { String } property
•	@param { Mixed } value
•	@param { String } message
Confirma que objeto tem propriedade direta ou herdada nomeada por property com um valor dado por value. 
Usa um igualdade rigorosa (===).
assert.propertyVal({ chá: 'é bom' }, 'chá', 'é bom');
 