preciso que você crie um to do list simples, que possa criar tarefas e marcar as mesmas como concluídas
Quero que você me envie o código de HTML, CSS e JS.
Preciso hospedar esse projeto no github, me de instruções completas com codigo e configuração do repositório.

Claro! Vou te ajudar com tudo: o código completo (HTML, CSS e JS) e as instruções para hospedar no GitHub. Vamos por partes:

---

## ✅ **1. Código do Projeto: To-Do List Simples**

### 🗂 Estrutura de Arquivos

Você pode criar uma pasta chamada `todo-list` com os seguintes arquivos:

```
todo-list/
│
├── index.html
├── styles.css
└── script.js
```

---

### 📄 `index.html`

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>To-Do List</title>
  <link rel="stylesheet" href="styles.css"/>
</head>
<body>
  <div class="container">
    <h1>Minha Lista de Tarefas</h1>
    <div class="input-group">
      <input type="text" id="taskInput" placeholder="Digite uma nova tarefa..." />
      <button onclick="addTask()">Adicionar</button>
    </div>
    <ul id="taskList"></ul>
  </div>

  <script src="script.js"></script>
</body>
</html>
```

---

### 🎨 `styles.css`

```css
body {
  font-family: Arial, sans-serif;
  background: #f4f4f4;
  display: flex;
  justify-content: center;
  padding-top: 50px;
}

.container {
  background: #fff;
  padding: 20px 30px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
  width: 100%;
  max-width: 400px;
}

h1 {
  text-align: center;
  color: #333;
}

.input-group {
  display: flex;
  margin-bottom: 20px;
}

#taskInput {
  flex: 1;
  padding: 10px;
  font-size: 16px;
}

button {
  padding: 10px 15px;
  background: #28a745;
  color: white;
  border: none;
  cursor: pointer;
}

button:hover {
  background: #218838;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  background: #f9f9f9;
  margin-bottom: 8px;
  padding: 10px;
  border-left: 5px solid #28a745;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

li.completed {
  text-decoration: line-through;
  color: #aaa;
  border-left: 5px solid #ccc;
}
```

---

### 💡 `script.js`

```javascript
function addTask() {
  const input = document.getElementById('taskInput');
  const taskText = input.value.trim();

  if (taskText === '') return;

  const li = document.createElement('li');
  li.textContent = taskText;
  li.onclick = function () {
    li.classList.toggle('completed');
  };

  document.getElementById('taskList').appendChild(li);
  input.value = '';
}
```

---

## 🌐 **2. Publicar no GitHub Pages**

### 📦 Crie um repositório no GitHub

1. Vá para [https://github.com](https://github.com).
2. Clique em **New repository**.
3. Nomeie como `todo-list` ou outro nome.
4. Marque **Public**.
5. Clique em **Create repository**.

---

### ⬆️ Subir o Projeto com Git

No terminal/cmd/prompt:

```bash
# Clone o repositório para sua máquina
git clone https://github.com/SEU_USUARIO/todo-list.git
cd todo-list

# Copie os arquivos (index.html, styles.css, script.js) para essa pasta
# Se já estiverem lá, pule este passo.

# Adicione os arquivos
git add .

# Commit das mudanças
git commit -m "Add To-Do List básico"

# Envie para o GitHub
git push origin main
```

---

### 🚀 Ativar o GitHub Pages

1. Vá no repositório no GitHub.
2. Clique em **Settings** > **Pages**.
3. Em "Source", escolha a branch `main` e a pasta `/root`.
4. Clique em **Save**.
5. O GitHub vai gerar um link do tipo:

```
https://seu-usuario.github.io/todo-list/
```

---

Se quiser, posso gerar o projeto como um `.zip` ou criar um repositório base para você clonar.

Deseja que eu prepare isso pra você?
