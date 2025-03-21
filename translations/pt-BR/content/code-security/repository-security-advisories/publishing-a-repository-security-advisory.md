---
title: Publishing a repository security advisory
intro: Você pode publicar uma consultoria de segurança para alertar a sua comunidade sobre uma vulnerabilidade de segurança no seu projeto.
redirect_from:
  - /articles/publishing-a-maintainer-security-advisory
  - /github/managing-security-vulnerabilities/publishing-a-maintainer-security-advisory
  - /github/managing-security-vulnerabilities/publishing-a-security-advisory
  - /code-security/security-advisories/publishing-a-security-advisory
versions:
  fpt: '*'
  ghec: '*'
type: how_to
topics:
  - Security advisories
  - Vulnerabilities
  - CVEs
  - Repositories
shortTitle: Publish repository advisories
---

<!--Marketing-LINK: From /features/security/software-supply-chain page "Publishing a security advisory".-->

Qualquer pessoa com permissão de administrador para um consultor de segurança pode publicar a consultoria de segurança.

{% data reusables.security-advisory.repository-level-advisory-note %}

## Pré-requisitos

Antes de publicar uma consultoria de segurança ou solicitar um número de identificação CVE, você deve criar um rascunho da consultoria de segurança e fornecer informações sobre as versões do seu projeto afetadas pela vulnerabilidade de segurança. For more information, see "[Creating a repository security advisory](/code-security/repository-security-advisories/creating-a-repository-security-advisory)."

Se você criou uma consultoria de segurança, mas ainda não forneceu as informações sobre as versões do seu projeto que a vulnerabilidade de segurança afeta, você pode editar a consultoria de segurança. For more information, see "[Editing a repository security advisory](/code-security/repository-security-advisories/editing-a-repository-security-advisory)."

## Sobre a publicação de uma consultoria de segurança

Ao publicar uma consultoria de segurança, você notifica a sua comunidade sobre a vulnerabilidade de segurança que a consultoria de segurança aborda. A publicação de uma consultoria de segurança torna mais fácil para a sua comunidade atualizar as dependências do pacote e pesquisar o impacto da vulnerabilidade de segurança.

{% data reusables.repositories.security-advisories-republishing %}

Antes de publicar uma consultoria de segurança, você pode colaborar de forma privada para consertar a vulnerabilidade em uma bifurcação privada temporária. For more information, see "[Collaborating in a temporary private fork to resolve a repository security vulnerability](/code-security/repository-security-advisories/collaborating-in-a-temporary-private-fork-to-resolve-a-repository-security-vulnerability)."

{% warning %}

**Aviso**: Sempre que possível, você deve adicionar uma versão de correção a uma consultoria de segurança antes de publicá-la. Se você não fizer isso, a sua consultoria será publicado sem uma versão de correção e {% data variables.product.prodname_dependabot %} alertará os seus usuários sobre o problema, sem oferecer qualquer versão segura para a qual atualizar.

Recomendamos que você tome as seguintes medidas nestas situações diferentes:

- Se uma versão de correção estiver disponível imediatamente, e você puder, espere para divulgar o problema quando a correção estiver pronta.
- Se uma versão de correção estiver em desenvolvimento mas ainda não disponível, mencione isso no consultor e edite a consultoria mais tarde, após a publicação.
- Se você não está planejando corrigir o problema, tenha isso claro na consultoria para que os usuários não entrem em contato com você para perguntar quando será feita uma correção. Neste caso, é útil incluir as etapas que os usuários podem seguir para mitigar o problema.

{% endwarning %}

Ao publicar um rascunho de consultoria a partir de um repositório público, todos poderão ver:

- A versão atual dos dados da consultoria.
- Todos os créditos da consultoria que os usuários creditados aceitaram.

{% note %}

**Observação**: O público em geral nunca terá acesso ao histórico de edição da consultoria e só verá a versão publicada.

{% endnote %}

Depois de publicar uma consultoria de segurança, sua URL permanecerá a mesma de antes da publicação da consultoria de segurança. Qualquer pessoa com acesso de leitura ao repositório pode ver a consultoria de segurança. Os colaboradores na consultoria de segurança podem continuar a visualizar conversas anteriores, incluindo o fluxo de comentários completo na consultoria de segurança, a menos que alguém com permissões de administração remova o colaborador da consultoria de segurança.

Se você precisar atualizar ou corrigir informações em uma consultoria de segurança que publicou, poderá editar a consultoria de segurança. For more information, see "[Editing a repository security advisory](/code-security/repository-security-advisories/editing-a-repository-security-advisory)."

## Publicar uma consultoria de segurança

A publicação de uma consultor de segurança elimina a bifurcação privada temporária para a consultoria de segurança.

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-security %}
{% data reusables.repositories.sidebar-advisories %}
4. Na lista "consultoria de segurança", clique na consultoria de segurança que deseja publicar. ![Consultoria de segurança na lista](/assets/images/help/security/security-advisory-in-list.png)
5. Na parte inferior da página, clique em **Publicar consultoria**. ![Botão Publish advisory (Publicar consultoria)](/assets/images/help/security/publish-advisory-button.png)

## {% data variables.product.prodname_dependabot_alerts %} para o aviso de segurança publicado

{% data reusables.repositories.github-reviews-security-advisories %}

## Solicitando um número de identificação CVE (Opcional)

{% data reusables.repositories.request-security-advisory-cve-id %} For more information, see "[About {% data variables.product.prodname_security_advisories %} for repositories](/code-security/repository-security-advisories/about-github-security-advisories-for-repositories#cve-identification-numbers)."

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-security %}
{% data reusables.repositories.sidebar-advisories %}
4. Na lista "consultoria de segurança", clique na consultoria de segurança para o qual deseja solicitar um número de identificação CVE. ![Consultoria de segurança na lista](/assets/images/help/security/security-advisory-in-list.png)
5. Use o menu suspenso **Publicar consultoria** e clique em **Solicitar CVE**. ![Solicitar CVE no menu suspenso](/assets/images/help/security/security-advisory-drop-down-request-cve.png)
6. Clique **Solicitar CVE**. ![Botão "Solicitar CVE"](/assets/images/help/security/security-advisory-request-cve-button.png)

## Leia mais

- "[Withdrawing a repository security advisory](/code-security/repository-security-advisories/withdrawing-a-repository-security-advisory)"
