# SSO / SAML

## Définition
Single Sign-On : permettre aux utilisateurs entreprise de se connecter avec leur compte professionnel (Google Workspace, Microsoft 365, Okta, etc.) sans créer un nouveau mot de passe.

## Sous-features

- [ ] SSO via Google Workspace
- [ ] SSO via Microsoft Entra ID (Azure AD)
- [ ] SAML 2.0
- [ ] OpenID Connect (OIDC)
- [ ] Provisioning automatique (SCIM)
- [ ] Just-in-Time provisioning
- [ ] Mapping de rôles depuis l'IdP
- [ ] Forced SSO (désactiver la connexion par mot de passe)

## Questionnaire de cadrage

1. Quels identity providers faut-il supporter ? (Google, Microsoft, Okta, custom)
2. Le SSO est-il disponible pour tous les plans ou réservé aux plans entreprise ?
3. Faut-il du provisioning automatique (SCIM) ? (création/suppression automatique de comptes)
4. Faut-il forcer le SSO (interdire la connexion par mot de passe) pour certaines organisations ?
5. Comment les rôles sont-ils mappés depuis l'IdP ? (groupes → rôles dans l'app)
6. Quel protocole ? (SAML 2.0, OIDC, les deux)
7. Qui configure le SSO ? (l'admin de l'organisation, le support)
