# pancakeswap-ico-testnet-bsc
Como executar o processo de ICO de tokens ERC20 na testnet da BSC utilizando o router da PancakeSwap

# Requisitos
- Ter um contrato estruturado adequadamente para o ICO
- Obter BNB com a Binance Smart Chain Faucet (https://testnet.binance.org/faucet-smart)
- Adicionar um endpoint RPC para a testnet em seu nó local(metamask)

# Adicionando o endpoint da testnet na metamask
Acesse https://testnet.bscscan.com/ e desça até o rodapé, no canto inferior direito verá: "Add BSC Network" e complete a autenticação e a confirmação solicitada pelo metamask.
(se você souber o que está fazendo, você pode também adicionar manualmente um endpoint para a testnet de moralis ou qualquer outro da sua preferencia)

# Adequação do contrato no remix
Com o contrato adequado em mãos, crie um arquivo cujo nome seja referente á sua utilidade ou token(não necessáriamente dessa forma, o nome não vai intervir. Mas é importante manter a organização). Neste caso, estou utilizando um código fork da Shiba INU (Sim, Shiba INU está na rede Ethereum mas caracterizamos a compatibilidade com a EVM e deste modo ambos utilizam os mesmos padrões). O codigo da Shiba INU está na versão 0.5.* então vá e altere caso apite erro.


# Deploy and runs
Antes de seguir este passo, certifique-se de que seu nó local está conectado á testnet:     ![image](https://user-images.githubusercontent.com/93963677/157054297-37b92041-1ec5-4444-bae5-5f59529de859.png)

Certifique-se de que o seu contrato foi compilado (normalmente é o segundo icone do remix "Solidity compiler" caso tenha sido compilado aparecerá um icone verde sobrepondo o o mesmo icone)

Desloque-se até o icone com o formato de Ether: "Deploys and run transactions" e na barrinha com rolagem, abaixo de Enviroment selecione Injected Web3 e mantenha as outras por default (altere se você souber o que está fazendo). Faça o deploy, gere o contrato e guarde-o.

# Injeção de liquidez na DEX
A principio, certifique-se de adquirir BNB no faucet da testnet. A partir daqui, acesse https://pancake.kiemtienonline360.com/#/pool pois o mesmo é uma copia do pancakeswap porém oferece uma interação com um router identico a mesma, existente na testnet.
Vale ressaltar que nunca é seguro fornecer a conexão do seu nó local a quaisquer sites então faça-o somente se quiser.

Após conectado seu nó local(metamask) no site, verá um grande botão estampado de azul "Add Liquidity" clique-o. Em um dos campos será fornecido o endereço do contrato do token gerado, e em outro campo será fornecido o Token B da liquidez (Token A=ERC20Token, Token B=Pair). Execute os passos necessários, como aprovação do acesso para o roteador acessar as quantias tokens para ICO, execute a injeção de liquidez e "voa-la", aqui está a ICO em uma testnet. A partir deste ponto você pode falar para seus amigos ou você mesmo poderá comprar/vender suas tokens em https://pancake.kiemtienonline360.com/#/swap

