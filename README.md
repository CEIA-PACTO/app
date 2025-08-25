# app
Repository created for the development of a homolog version of the form application and secure deployment of the application.

## 📑 Sumário
- [App](#app)
- [Como Executar](#-como-executar)
- [Documentação de endpoints](#-documentação-de-endpoints)

---

## 🔧 Como Executar

### 1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/Squad-ai.git
cd Squad-ai
```

### 2. Crie e ative o ambiente virtual
```bash
python -m venv .venv
source .venv/bin/activate  # Linux/macOS
.venv\Scripts\activate     # Windows
```

### 3. Instale as dependências
```bash
pip install -r requirements.txt
```
### 4. Execução local
```
# backend
uvicorn src.backend:app --reload

# app
streamlit run src/app.py
```
### 4.1. Execução com Docker
```
# Docker build - (1 container com Supervisor)
docker build -t squad-app .
docker run -p 9000:8000 squad-app

# Docker-compose - (serviços separados)
docker-compose up --build
```

## 📘 Documentação de endpoints
Pagina swagger 
```
http://localhost:8000/docs
```