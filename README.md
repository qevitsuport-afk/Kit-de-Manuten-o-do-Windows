# Kit de Manutenção do Windows 11

Scripts gratuitos de diagnóstico, verificação e reparação para Windows 11, criados pela [QEVIT SUPORT](https://qevitsuport.blogspot.com/).

> Artigo completo com explicações: https://qevitsuport.blogspot.com/2026/11/kit-manutencao-windows-11-scripts.html

## Conteúdo

| Ficheiro | Descrição |
|---|---|
| `scripts/diagnostico_windows11.ps1` | Diagnóstico do Windows 11: sistema, memória RAM, armazenamento e rede (PowerShell). |
| `scripts/reparar_imagem_windows11.ps1` | Reparação opcional com DISM e SFC (requer Administrador). |
| `scripts/relatorio_diagnostico.py` | Relatório multiplataforma: sistema operativo, arquitetura, processador e disco (Python 3). |
| `scripts/diagnostico.sh` | Diagnóstico básico para Linux e macOS (shell). |
| `LEIA_ANTES_DE_EXECUTAR.txt` | Instruções a ler antes de usar. |

> Ajuste os nomes da tabela aos ficheiros reais do kit.

## Requisitos

- Windows 11 (scripts `.ps1`)
- PowerShell 5.1 ou posterior
- Python 3 (relatório multiplataforma)
- macOS ou Linux (script shell)
- Privilégios de Administrador (apenas para a reparação)

## Como usar

1. Descarregue o ZIP na secção **Releases** deste repositório (ou use *Code > Download ZIP*).
2. Verifique o hash (opcional, mas recomendado):

   ```powershell
   Get-FileHash .\NOME-DO-ZIP.zip -Algorithm SHA256
   ```

   Hash SHA-256 da versão 1.0: `COLOCAR_HASH_SHA256`

3. Extraia o ZIP, leia o código dos scripts e desbloqueie-os:

   ```powershell
   Get-ChildItem .\scripts\*.ps1 | Unblock-File
   ```

4. Execute o diagnóstico:

   ```powershell
   powershell -NoProfile -ExecutionPolicy RemoteSigned -File .\scripts\diagnostico_windows11.ps1
   ```

5. Se necessário, abra o PowerShell **como Administrador** e execute a reparação:

   ```powershell
   powershell -NoProfile -ExecutionPolicy RemoteSigned -File .\scripts\reparar_imagem_windows11.ps1
   ```

   O script pede confirmação antes de iniciar a sequência DISM e SFC, que pode demorar vários minutos.

## Aviso de segurança

- Faça uma cópia de segurança dos dados importantes e, se possível, crie um ponto de restauro antes de usar a reparação.
- Leia o código antes de executar qualquer script.
- Não desative o antivírus e não execute ficheiros de origem desconhecida.
- Este software é fornecido "como está", sem garantias, e não substitui uma avaliação técnica profissional.

## Contribuir e reportar problemas

Encontrou um erro ou tem uma sugestão? Abra uma [Issue](../../issues) ou envie um Pull Request.

## Contacto

- WhatsApp: [+244 955 801 690](https://wa.me/244955801690)
- E-mail: qevitsuport@gmail.com
- Site: https://qevitsuport.blogspot.com/

## Licença

Distribuído sob a licença MIT. Consulte o ficheiro [LICENSE](LICENSE).
