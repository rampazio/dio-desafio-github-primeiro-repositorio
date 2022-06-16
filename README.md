# Lista de comandos, lembretes e consultas rápidas.
Repositorio criado para o desafio de Projeto.

## Links Úteis
[Sintaxe Basica Markdows](https://www.markdownguide.org/basic-syntax/)


## Comandos Git.

- git config --global user.name "rampazio" (Configura o nome do usuário)
- git config --global user.email "seu email cadastrado no git" ( Configurar e-mail)
- git init (iniciar repositorio no projeto)
- git add . (adicionar os arquivos para salvar)
- git status (verifica status dos arquivos)
- git commit -m "menssagem" (salva os arquivos no commit com uma menssage)
- git log --oneline ( lista historico de versões salvas)
- git remote ... (associa o projeto com do git hub)
- git remote add origin git@github.com:usuário/nome do projeto (associa projeto com sua conta do github)
- git remote -v ( confirma os dados de envio do projeto)
- git branch -M main (Muda o nome da Branch para main, alguns casos fica como master e pode dar erro)
- git push -u origin main ( envia o projeto para o github)

## Comandos para o SSH

- $ ssh-keygen -t rsa -b 4096 -C "email_do_github" (colocar email para gerar ssh)
- $ eval "${ssh-agent -s}" (iniciar agent ssh)
- Agent pid 59566  (selecionar ssh)
- $ ssh-add ~/.ssh/id_rsa (adicionar ssh local)
- $ git remote -v  (verificar conta)
- $ git remote set-url origin git@github.com:andgomes/my-repo.git ( relacionar ssh ao repositorio git hub)

Fonte : [https://medium.com/@andgomes/git-github-evitando-informar-usu%C3%A1rio-e-senha-a-cada-push-para-o-github-d8edbb5c6de4](https://medium.com/@andgomes/git-github-evitando-informar-usu%C3%A1rio-e-senha-a-cada-push-para-o-github-d8edbb5c6de4) 

## Comandos dotnet.


- mkdir  "nome"                            ( Criar diretorio. )
- dotnet new sln --name ExemploPPO         ( Cria uma solução. )
- dotnet sln add  caminho do projeto       ( Adiciona o projeto a solução. )
- dotnet new console -n nome do projeto    ( Cria um novo projeto com o nome desejado.  )
- dotnet restore                           ( Restaura os pacotes. )
- dotnet build                             ( Processo de compilação gerando os binarios. )
- dotnet run                               ( Executa a build. ) 
- code .                                   ( abre o vs code. )
- explorer .                               ( abre o explorer do windows.)

## Comandos yarn.

- yarn start ( Inicia o yarn[para parar, usar teclas Ctrl+C])
- yarn add react-router-dom@6.2.1 @types/react-router-dom@5.3.2 (Instala rotas nas pastas)









# modelos


## Modelo configuração de rotas página principal
import {
  BrowserRouter,
  Routes,
  Route
} from "react-router-dom";
import Listing from 'pages/Listing';
import Form from 'pages/Form';
import Navbar from "components/Navbar";

function App() {
  return (
    <BrowserRouter>
      <Navbar />
      <Routes>
        <Route path="/" element={<Listing />} />
        <Route path="/form">
          <Route path=":movieId" element={<Form />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
}

export default App;


