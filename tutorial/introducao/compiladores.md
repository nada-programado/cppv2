# Compiladores

As ferramentas essenciais necessárias para seguir esses tutoriais são um computador e uma cadeia de ferramentas de compilação capaz de compilar códigos C++ e construir os programas para serem executados nele.

C++ é uma linguagem que evoluiu muito ao longo dos anos, e esses tutoriais explicam muitos recursos adicionados recentemente à linguagem. Portanto, para seguir corretamente os tutoriais, é necessário um compilador recente. Ele deve suportar (mesmo que apenas parcialmente) os recursos introduzidos pelo padrão 2011.

Muitos fornecedores de compiladores suportam os novos recursos em diferentes graus. Veja na parte inferior desta página alguns compiladores que são conhecidos por oferecer suporte aos recursos necessários. Alguns deles são gratuitos!

Se por algum motivo você precisar usar algum compilador mais antigo, você pode acessar uma versão mais antiga desses tutoriais aqui (que não tem atualizações).

## O que é um compilador?

Os computadores entendem apenas uma linguagem e essa linguagem consiste em conjuntos de instruções feitas de uns e zeros. Essa linguagem do computador é apropriadamente chamada de linguagem de máquina.

Uma única instrução para um computador pode ser assim:

```
00000 100111110
```

O programa de linguagem de máquina de um computador específico que permite ao usuário inserir dois números, somar os dois números e exibir o total pode incluir estas instruções de código de máquina:

```
00000 | 10011110
00001 | 11110100
00010 | 10011110
00011 | 11010100
00100 | 10111111
00101 | 00000000
```

Como você pode imaginar, programar um computador diretamente em linguagem de máquina usando apenas uns e zeros é muito tedioso e propenso a erros. Para facilitar a programação, foram desenvolvidas linguagens de alto nível. Programas de alto nível também tornam mais fácil para os programadores inspecionarem e entenderem os programas uns dos outros.

Esta é uma parte do código escrito em C++ que cumpre exatamente o mesmo propósito:

```cpp
int a, b, sum;

cin >> a;
cin >> b;

sum = a + b;
cout << sum << endl;
```

Mesmo que você não consiga realmente entender o código acima, você deve ser capaz de apreciar como será mais fácil programar na linguagem C++ em oposição à linguagem de máquina.

Como um computador só pode entender a linguagem de máquina e os humanos desejam escrever em linguagens de alto nível, as linguagens de alto nível precisam ser reescritas (traduzidas) em linguagem de máquina em algum momento. Isso é feito por programas especiais chamados compiladores, interpretadores ou montadores (assemblers) que são incorporados aos vários aplicativos de programação.

C++ foi projetado para ser uma linguagem compilada, o que significa que geralmente é traduzido em linguagem de máquina que pode ser entendida diretamente pelo sistema, tornando o programa gerado altamente eficiente. Para isso, é necessário um conjunto de ferramentas, conhecidos como *toolchain* de desenvolvimento, cujo o núcleo é um compilador e seu *linker*.

## Programas de console

Programas de console são programas que usam texto para se comunicar com o usuário e o ambiente, como imprimir texto na tela ou ler a entrada de um teclado.

Os programas de console são fáceis de interagir e geralmente têm um comportamento previsível que é idêntico em todas as plataformas. Eles também são simples de implementar e, portanto, são muito úteis para aprender o básico de uma linguagem de programação: Os exemplos nestes tutoriais são todos programas de console.

A maneira de compilar programas de console depende da ferramenta específica que você está usando.

A maneira mais fácil para os iniciantes compilarem programas C++ é usando um Ambiente de Desenvolvimento Integrado (IDE). Um IDE geralmente integra várias ferramentas de desenvolvimento, incluindo um editor de texto e ferramentas para compilar programas diretamente dele.

Aqui você tem instruções sobre como compilar e executar programas de console usando diferentes interfaces desenvolvimento integrado (IDEs) gratuitas:

OBS: Depois transformar isso em tabela, e consultar a referência de compiladores em https://www.cplusplus.com/doc/tutorial/introduction/

| IDE                   | Plataforma          | Programas de console                                                                                                      |
| --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Code::blocks          | Windows/Linux/macOS | [Compilando programas de console usando Code::blocks](https://cplusplus.com/doc/tutorial/introduction/codeblocks/)        |
| Visual Studio Express | Windows             | [Compilando programas de console usando o VS Express 2013](https://cplusplus.com/doc/tutorial/introduction/visualstudio/) |
| Dev-C++               | Windows             | [Compilando programas de console usando Dev-C++](https://cplusplus.com/doc/tutorial/introduction/devcpp/)                 |

Se você estiver em um ambiente Linux ou Mac com recursos de desenvolvimento, poderá compilar qualquer um dos exemplos diretamente de um terminal apenas incluindo sinalizadores C++ 11 no comando para o compilador:

| Compilador | Plataforma             | Comando                                                             |
| ---------- | ---------------------- | ------------------------------------------------------------------- |
| GCC        | Linux, e alguns outros | `g++ -std=c++0x exemplo.cpp -o programa_exemplo`                    |
| Clang      | OS X, alguns outros    | `clang++ -std=c++11 -stdlib=libc++ exemplo.cpp -o programa_exemplo` |
