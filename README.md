# MER - Osvaldo Motors
 
### Entidades e atributos
 
#### 🧑 CLIENTE
 
* id_cliente (PK)
* nome
#### 🚗 CARRO
 
* id_carro (PK)
* placa
* modelo
* marca
* id_cliente (FK)
#### 🔧 SERVICO
 
* id_servico (PK)
* nome
* preco
#### 📋 ORDEM_SERVICO
 
* id_os (PK)
* data
* pago
* conferido
* id_carro (FK)
#### ✅ ITEM_OS
 
* id_item (PK)
* realizado
* id_os (FK)
* id_servico (FK)
### Relacionamentos
 
* 1 CLIENTE possui N CARROS (1:N)
* 1 CARRO tem N ORDENS_SERVICO (1:N)
* 1 ORDEM_SERVICO possui N ITEM_OS (1:N)
* 1 SERVICO aparece em N ITEM_OS (1:N)
### RN's
 
* Se marca = BMW, Audi ou Mercedes → preço exibido = preco × 1,20 (REQ06)
* O carro só é liberado se pago e conferido (REQ10 e REQ11)
* Somente o proprietário altera preços (REQ04, REQ08 e REQ09)

