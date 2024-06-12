## [DIO] - Trilha Java Básico

## POO - Desafio

### Modelagem e Diagramação de um Componente iPhone

Neste desafio, você será responsável por modelar e diagramar a representação UML do componente iPhone, abrangendo suas funcionalidades como Reprodutor Musical, Aparelho Telefônico e Navegador na Internet.

#### Contexto
Com base no vídeo de lançamento do iPhone de 2007 (link abaixo), você deve elaborar a diagramação das classes e interfaces utilizando uma ferramenta UML de sua preferência. Em seguida, implemente as classes e interfaces no formato de arquivos `.java`.

[Lançamento iPhone 2007](https://www.youtube.com/watch?v=9ou608QQRq8)
- Minutos relevantes: 00:15 até 00:55

#### Funcionalidades a Modelar
1. **Reprodutor Musical**
   - Métodos: `tocar()`, `pausar()`, `selecionarMusica(String musica)`
2. **Aparelho Telefônico**
   - Métodos: `ligar(String numero)`, `atender()`, `iniciarCorreioVoz()`
3. **Navegador na Internet**
   - Métodos: `exibirPagina(String url)`, `adicionarNovaAba()`, `atualizarPagina()`

### Objetivo
1. Criar um diagrama UML que represente as funcionalidades descritas acima.
2. Implementar as classes e interfaces correspondentes em Java (Opcional).

# Diagrama UML (Mermaid) feito por Leandro Coelho
```mermaid
classDiagram
    class iPhone {
        -apps: List < App >
        -battery: batteryLevel
        +addApp(app: App) void
        +removeApp(app: App) void
        +chargeBattery() void
    
    }
    
    class iTunes {
        -Reproduzir: List < Media >
        +tocar() void
        +pausar() void
        +selecionarMusica() void
        +volumeAumentar() void
        +volumeDiminuir() void
    }

    class Musica {
        nome String
        artista String
        caminho String

    }

    class Video {
        nome String
        artista String
        caminho String

    }

    class Foto {
        nome String
        caminho String

    }

    class Phone {
        -Contatos: list < Contato >
        -redeMovelDisponivel() Boolean
        +ligar(numero: String) void
        +atender() void
        +iniciarCorreioVoz() void
    }

    class Contato {
        nome String
        numero String

    }

    class Safari {
        -paginaInicial: String
        -historico: List < String >
        -conexaoComInternet() Boolean
        +exibirPagina(url) String
        +adicionarNovaAba() void
        +atualizarPagina() void
        +voltar() void
    }   

    iPhone ..|> iTunes
    iPhone ..|> Phone
    iPhone ..|> Safari
    iTunes ..|> Musica
    iTunes ..|> Video
    iTunes ..|> Foto
    Phone ..|> Contato
    ```

    [![](https://mermaid.ink/img/pako:eNq1VNtu2zAM_RXDTyl6-QBjKJAmGFCgGYpl6FNeGIm1icmiIUtGmy7_PsZyU6cy0r3MQAL6UCbFc0i-5Yo15kWuDLTtkqB0UG9sJk-PZPRYscXsLWKH5xqapi2yB2p99i2bN012O3JuwXt0r0U2GA_YofnwX4LW8slMYhSHby-yjkmP_A5r7vDsEVWBK_Euxp-N3fF_P34ZqvgVLLYnVfzExrEOO3LHWlaoCcbVXHpW4GbJDRoI7RTeokFFbMGtQksK0hMdm1DjXH7WT0WI_iXVZAOd-qWscUkxw7gkyzVma-_Ilh8gOC_FQYIrkBQVH_HJHE-kkf9viu_sv87wT5HSRl2wkOxZmtVEgQfgpGEdalxJy5kltQ1bEktov2M2CHakjKFSBLOijuNiuEkiH3i0Gid0JUuKwC3YOSR-4t05ad-v-RUt8TLnWVnDMzg6oaWBkizc9zcyRRL1uhKy2JHi42DEIye0KSH7BXjB9b2VObToJ1nDF9qSe-wzzoIzF0k62QgUZ-YHdzDfTgwN-ACGdvAeZ2pqPk_Tvt8A0R522M3Nn9thE6R4b6ZwpG_A4xLp8Th9Kd5PTAofujyio9iDzPlVLjLWQFrWcK_TJvcV1rjJCzE1uN-bfGP3cg6C5_WrVXnhXcCr3HEoq7x4BtPKW2i09N-wwwd0_xcwVcxw?type=png)](https://mermaid.live/edit#pako:eNq1VNtu2zAM_RXDTyl6-QBjKJAmGFCgGYpl6FNeGIm1icmiIUtGmy7_PsZyU6cy0r3MQAL6UCbFc0i-5Yo15kWuDLTtkqB0UG9sJk-PZPRYscXsLWKH5xqapi2yB2p99i2bN012O3JuwXt0r0U2GA_YofnwX4LW8slMYhSHby-yjkmP_A5r7vDsEVWBK_Euxp-N3fF_P34ZqvgVLLYnVfzExrEOO3LHWlaoCcbVXHpW4GbJDRoI7RTeokFFbMGtQksK0hMdm1DjXH7WT0WI_iXVZAOd-qWscUkxw7gkyzVma-_Ilh8gOC_FQYIrkBQVH_HJHE-kkf9viu_sv87wT5HSRl2wkOxZmtVEgQfgpGEdalxJy5kltQ1bEktov2M2CHakjKFSBLOijuNiuEkiH3i0Gid0JUuKwC3YOSR-4t05ad-v-RUt8TLnWVnDMzg6oaWBkizc9zcyRRL1uhKy2JHi42DEIye0KSH7BXjB9b2VObToJ1nDF9qSe-wzzoIzF0k62QgUZ-YHdzDfTgwN-ACGdvAeZ2pqPk_Tvt8A0R522M3Nn9thE6R4b6ZwpG_A4xLp8Th9Kd5PTAofujyio9iDzPlVLjLWQFrWcK_TJvcV1rjJCzE1uN-bfGP3cg6C5_WrVXnhXcCr3HEoq7x4BtPKW2i09N-wwwd0_xcwVcxw)

    ### FIM


