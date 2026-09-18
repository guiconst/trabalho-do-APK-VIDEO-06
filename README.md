# 📱 CI/CD Demo App - Build Automático de APK

> Projeto demonstrativo de pipeline CI/CD usando **GitHub Actions** para gerar automaticamente um APK Android a cada push.

## 🎯 Sobre o Projeto

Este é um aplicativo Android simples (Hello World) criado para demonstrar na prática o funcionamento de um pipeline de **Integração Contínua / Entrega Contínua (CI/CD)**.

**Tecnologias utilizadas:**
- **Android** (Kotlin) — Código-fonte do app
- **Gradle** — Sistema de build
- **GitHub Actions** — Automação CI/CD

## 🔄 Como o Pipeline CI/CD Funciona

```
Push no GitHub → GitHub Actions detecta → Configura ambiente → Compila o app → Gera APK → Disponibiliza para download
```

### Fluxo detalhado:

1. **Desenvolvedor faz push** na branch `main`
2. **GitHub Actions** é acionado automaticamente
3. O workflow configura:
   - ☕ JDK 17 (Java Development Kit)
   - 📋 Licenças do Android SDK
   - 🔧 Gradle 8.7 (ferramenta de build)
4. **Compila** o projeto Android (`gradle assembleDebug`)
5. **Gera o APK** de debug
6. **Faz upload** do APK como artifact, disponível para download na aba "Actions" do repositório

## 📦 Como Baixar o APK Gerado

1. Acesse a aba **Actions** no repositório do GitHub
2. Clique no workflow mais recente (✅ verde = sucesso)
3. Na seção **Artifacts**, clique em **app-debug-apk** para baixar o APK

## 🗂️ Estrutura do Projeto

```
├── .github/
│   └── workflows/
│       └── build-apk.yml          ← Workflow do GitHub Actions
├── app/
│   ├── build.gradle.kts           ← Configuração de build do app
│   └── src/main/
│       ├── AndroidManifest.xml    ← Manifesto do app
│       ├── java/.../MainActivity.kt  ← Código principal
│       └── res/                   ← Recursos (layouts, strings, cores)
├── build.gradle.kts               ← Build raiz do projeto
├── settings.gradle.kts            ← Configuração dos módulos
├── gradle.properties              ← Propriedades do Gradle
├── .gitignore                     ← Arquivos ignorados pelo Git
└── README.md                      ← Este arquivo
```

## 👨‍🎓 Contexto Acadêmico

Projeto desenvolvido como trabalho prático do curso técnico em **Desenvolvimento de Sistemas**, demonstrando o conceito de CI/CD aplicado ao desenvolvimento mobile Android.

---

*Feito com ❤️ para fins educacionais*
