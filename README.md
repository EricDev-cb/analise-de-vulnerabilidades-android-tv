# Analise de vulnerabilidades (Android TV)

## Resumo
Análise de segurança de uma TV stick Android da Tomate.
Identificadas falhas de configuração que permitem execução de código não autorizado.

## Ambiente
- Dispositivo: Tomate TV Stick (Android TV)
- Acesso: ADB, terminal local
- Método: Análise manual

## Descobertas

### 1. SELinux em modo permissive
- **Severidade:** Alta
- **Descrição:** O sistema registra comportamentos suspeitos mas não os bloqueia.
- **Impacto:** Atacante pode executar código arbitrário sem impedimento.

### 2. Acesso root por padrão
- **Severidade:** Alta
- **Descrição:** Acesso root habilitado de fábrica, sem senha.
- **Impacto:** Qualquer app ou acesso físico tem controle total do sistema.

### 3. Aplicativos pré-instalados suspeitos
- **Severidade:** Média
- **Descrição:** Apps com permissões excessivas e comunicação com servidores desconhecidos.

## Recomendações
- Ativar SELinux em enforcing
- Desabilitar root por padrão
- Auditar apps pré-instalados

## Lições aprendidas
- Diferença entre detecção e prevenção
- Análise de firmware Android
- Importância de threat modeling em IoT
