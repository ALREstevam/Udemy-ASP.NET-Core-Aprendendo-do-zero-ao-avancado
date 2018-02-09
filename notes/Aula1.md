# ASP.NET Core: Aprendendo do zero ao avançado (v 1.1 e 2.0)

# ***AULA 1***

## O que mudou no ASP.NET Core
**Se mudou, como era antes?**

* Antes do .NET Core existia o .NET Framework, nele:
	* Se usa ***WebForms*** que é muito parecido com os ***Windows Forms***
		* Possibilita criar a página sem ter que entender de HTML
	* A performance é um problema em ***WebForms***
	* Atualizações do *framework* demoravam e eram complicadas (por conta das dependências)
	* Existiam componentes semelhantes que não funcionavam da maneira esperada dependendo da plataforma alvo (duplicação de código). Exemplo:
	* Os repositórios ***.Net Framework*** para desktop e ***.Net Compact Framework*** para mobile tinham muitas classes com mesmo nome e comportamentos diferentes 
	* Funciona apenas no Windows
	* Mesmo na mesma plataforma, configurações são diferentes dependendo do alvo
	* O único editor que funciona é o Visual Studio (obrigatório)	

![https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/01.PNG?raw=true](https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/01.PNG?raw=true)

![https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/02.PNG?raw=true](https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/02.PNG?raw=true)

### .NET Core
Como a antiga plataforma não atendia muitos dos requisitos para que fosse usada por uma grande comunidade, a Microsoft criou uma nova plataforma do zero, o .NET Core.

## .NET Framework vs .NET Core
### Diferenças
![https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/03.PNG?raw=true](https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/03.PNG?raw=true)

O .NET Core é:
* Mais modular
	* Pedaços de código independentes que podem ser liberados por partes
	* Web Forms, MVC e Web API foram concentrados em ASP.NET Core MVC

## O que é o .NET Core?
![https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/04.PNG?raw=true](https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/04.PNG?raw=true)

* Modularizado, cada componente é distribuído através do NuGet, o gerenciador de bibliotecas da Microsoft, hoje ele gerencia apenas as bibliotecas do .NET Core, as bibliotecas clients podem ser gerenciadas por outro gerenciador
* Os aplicativos rodam independentemente da versão do ASP.NET Core no servidor pois levam consigo o que precisam para serem rodados, ou seja, o projeto leva a versão do framework.
* É cross-platform
* É open-source e pode ser acessado pelo GitHub
* Funciona com qualquer editor e ferramenta (já que é cross-platform)

## Novas features
* Kestrel
	* É um web server para ASP.NET Core baseado no libuv, um cross-platform asynchonous I/O library. O Kestrel é um web server incluído por default no ASP.NET Core
	* ![https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/05.PNG?raw=true](https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/05.PNG?raw=true)
	* Em alguns cases o desempenho quando comparado ao node.js tem um desempenho 3 vezes mais rápido
	* > libuv foi feito para node.js e outros web services estão o utilizando como base, assim como o Kestrel
	* Responsável pelo hosting do .NET Core 
* Middleware
* Dependency Injection
	* O ASP.NET Core tem o próprio injetor de dependências mas que que pode ser trocado por outro container 
* Configuration
	* No antigo ASP, 80% das configurações num WebConfig eram do framework e apenas 20% eram de fato o que a aplicação usaria
	* Deixaram de utilizar XML e passaram a usar JSON e nele ficarão apenas as configurações da aplicação e não do framework


### Velocidade
![https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/06.PNG?raw=true](https://github.com/ALREstevam/Udemy-ASP.NET-Core-Aprendendo-do-zero-ao-avancado/blob/master/Images/06.PNG?raw=true)


### .NET Framework vs .NET Core, qual usar?
**Use o .NET Core se:**
* É uma nova aplicação
* Precisa ser cross-platform
* Usa Microservices
* Usa Docker Containers
* Precisa de alta performance e sistemas escaláveis
* Versão do .NET no lado da aplicação

**Use o .NET Framework se:**
* Sua aplicação já o usa
* Precisa de bibliotecas de terceiros que não estão disponíveis para o .NET Core
* Utiliza de tecnologias de terceiros que não estão disponíveis para o .NET Core