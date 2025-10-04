# 🚗 App Motorista - Sua Empresa

Sistema web para gestão de corridas por motoristas, com registro de localização, exportação de planilhas, PWA e integração com Firebase.

---

## 📱 Funcionalidades Principais

- **Login rápido:** Nome e PIN simples para uso pelos motoristas.
- **Registro de localização:** Geolocalização em tempo real, com histórico.
- **Cadastro de corridas:** Valor, hora e localização salvos no Firestore.
- **Listagem do dia:** Veja todas as corridas feitas no dia, com totalizador.
- **Exportação para CSV:** Gere planilhas em um clique.
- **Funciona offline:** App PWA, instala e roda sem internet.
- **Deploy fácil:** Netlify ou GitHub Pages.
- **Totalmente customizável:** Ajuste cores, textos e logo facilmente.

---

## 🚀 Instalação & Deploy

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/app-motorista-completo.git
cd app-motorista-completo
```

### 2. Configure o Firebase

- Crie um projeto no [Firebase Console](https://console.firebase.google.com)
- Ative o **Firestore Database** (modo de teste na região `southamerica-east1`)
- Em "Configurações do Projeto" > "Seus apps" > Web, copie as credenciais
- Cole as credenciais em `src/js/firebase.js` no objeto `firebaseConfig`

### 3. Deploy (opcional)

#### Netlify (Recomendado)

- Arraste a pasta do projeto em [Netlify Drop](https://app.netlify.com/drop)
- Ou use o CLI:  
  ```bash
  npm install -g netlify-cli
  netlify deploy
  ```

#### GitHub Pages

- Suba para um repositório GitHub
- Vá em Settings > Pages > "Deploy from branch" (main ou docs)
- Acesse o link gerado

---

## 🖥️ Estrutura de Pastas

```
/
├── index.html
├── manifest.json
├── sw.js
├── README.md
├── /src
│   ├── /js
│   │   ├── app.js
│   │   └── firebase.js
│   └── /css
│       └── styles.css
└── /assets
    ├── /icons
    └── /images
```

---

## 🎨 Personalização

- **Cores**: Edite as variáveis no topo de `src/css/styles.css`
- **Textos/Título**: Modifique `index.html`
- **Logo**: Substitua arquivos em `assets/icons/`
- **Nome do app e ícone de instalação**: Ajuste `manifest.json`

---

## 🔒 Segurança

- **Nunca exponha dados sensíveis** em produção.
- **Regras do Firestore**: Ajuste as regras para permitir apenas operações necessárias.
- **PIN não é seguro**: Para produção, use autenticação do Firebase (e-mail, telefone, etc).

---

## 💡 Dicas de Uso

1. O motorista acessa o link pelo celular e instala como PWA.
2. Faz login com nome e PIN.
3. Ativa a localização (necessário autorizar o navegador).
4. Registra corridas ao longo do dia.
5. Exporta a planilha quando desejar.
6. Faz logout ao terminar.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5, CSS3 (Bootstrap 5)**
- **JavaScript (ES6+, modularização sugerida)**
- **Firebase Firestore**
- **PWA (Service Worker, Manifest)**
- **Netlify/GitHub Pages (deploy)**

---

## 📸 Screenshots

> Coloque aqui imagens da tela de login, dashboard e exportação, por exemplo:

- ![Login](assets/prints/login.png)
- ![Dashboard](assets/prints/dashboard.png)

---

## 👨‍💻 Contribuindo

1. Faça um **fork** do projeto.
2. Crie uma branch (`git checkout -b feature/nova-funcionalidade`)
3. Commit as mudanças (`git commit -am 'feat: nova funcionalidade'`)
4. Push na branch (`git push origin feature/nova-funcionalidade`)
5. Abra um **Pull Request**

---

## ❓ FAQ

- **Não consigo ativar localização:**  
  Verifique permissões do navegador. Teste no Chrome/Edge no Android.

- **Erro no Firebase:**  
  Confira as credenciais, se o Firestore está ativo e as regras.

- **App não instala:**  
  Use um navegador compatível (Chrome, Edge). Clique no menu e depois em "Adicionar à tela inicial".

---

## 📝 Licença

MIT License - Veja o arquivo [LICENSE](LICENSE)

---

## 📬 Contato

Dúvidas ou sugestões?  
[Abra uma issue](https://github.com/seu-usuario/app-motorista-completo/issues) ou envie um e-mail para [seu-email@dominio.com](mailto:seu-email@dominio.com)
