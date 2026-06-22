# INDEX_PROJET.md — musejam

**Dossiers des plugins disponibles dans :** `C:\Users\Pierre\Documents\GitHub\temp\agents\plugins`

---

## 🎯 Contexte du projet

**Application légère monopage (HTML/JS Vanilla) avec :** Outil d'entraînement musical pour session live en improvisation.

**Stack technique :**
- HTML/CSS/JS pur (aucun framework)
- Web Audio API pour la restitution sonore
- Interface responsive et tactile
- Données musicales en mémoire (pas de SGBD)
- Un seul fichier `index.html`

**Fonctionnalités clés :**
- Générateur de progression d'accords
- Séquenceur rythmique interactif
- Métronome et playback audio
- Édition en direct des patterns
- Piano visuel avec feedback
- Contraintes et défis d'improvisation
- Mode "Doux / Medium / Spicy" pour la difficulté

---

## 📋 Agents retenus

---

### ACCESSIBILITY-COMPLIANCE

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/ui-visual-validator.md** | ➜ Déclencher après chaque modification UI majeure pour vérifier contraste, focus, et interactions tactiles | `accessibility-compliance/agents/ui-visual-validator.md` |
| **commands/accessibility-audit.md** | ➜ Utiliser avant une revue de code ou un push pour valider la conformité WCAG 2.1 AA (contraste, navigation clavier, échelles de zoom) | `accessibility-compliance/commands/accessibility-audit.md` |
| **skills/screen-reader-testing/SKILL.md** | ➜ Appliquer lors des tests manuels sur mobile (VoiceOver/TalkBack) pour valider l'expérience utilisateur non-voyante | `accessibility-compliance/skills/screen-reader-testing/SKILL.md` |
| **skills/wcag-audit-patterns/SKILL.md** | ➜ Utiliser pour valider les composants custom (boutons, sélecteurs, séquenceur) contre les règles WCAG 2.1 AA | `accessibility-compliance/skills/wcag-audit-patterns/SKILL.md` |

---

### APPLICATION-PERFORMANCE

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/frontend-developer.md** | ➜ Déclencher pour toute optimisation de rendu, gestion du DOM (rafraîchissement du séquenceur, mise à jour du piano) | `application-performance/agents/frontend-developer.md` |
| **commands/performance-optimization.md** | ➜ Lancer après avoir ajouté une nouvelle fonctionnalité animée ou interactive pour valider le maintien de 60fps | `application-performance/commands/performance-optimization.md` |

---

### CODE-DOCUMENTATION

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/code-reviewer.md** | ➜ Utiliser lors des revues de code pour vérifier la clarté et l'auto-documentation du code (fonctions nommées explicitement, variables claires) | `code-documentation/agents/code-reviewer.md` |
| **commands/code-explain.md** | ➜ Déclencher lorsqu'une fonction ou un bloc de code devient trop complexe (ex: gestion du scheduler audio, mapping des rythmes) | `code-documentation/commands/code-explain.md` |

---

### CODE-REFACTORING

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/code-reviewer.md** | ➜ Utiliser avant chaque refactoring pour identifier les opportunités de simplification (dette technique dans la logique musicale) | `code-refactoring/agents/code-reviewer.md` |
| **agents/legacy-modernizer.md** | ➜ Utiliser pour maintenir la codebase propre et modulaire, surtout avec l'accumulation de versions (V18) | `code-refactoring/agents/legacy-modernizer.md` |
| **commands/tech-debt.md** | ➜ Lancer périodiquement pour évaluer la dette technique accumulée (surtout le scheduler, le state management, et les callbacks DOM) | `code-refactoring/commands/tech-debt.md` |
| **commands/refactor-clean.md** | ➜ Utiliser avant d'ajouter une nouvelle fonctionnalité majeure pour nettoyer le code existant | `code-refactoring/commands/refactor-clean.md` |

---

### CODEBASE-CLEANUP

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/code-reviewer.md** | ➜ Utiliser pour identifier les fonctions mortes, variables inutilisées, et code redondant | `codebase-cleanup/agents/code-reviewer.md` |
| **commands/deps-audit.md** | ➜ Utiliser pour vérifier que le projet reste sans dépendances externes (sauf la police Google Fonts) | `codebase-cleanup/commands/deps-audit.md` |

---

### COMPREHENSIVE-REVIEW

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/code-reviewer.md** | ➜ Utiliser pour les revues de code approfondies avant les versions majeures (ex: V18 → V19) | `comprehensive-review/agents/code-reviewer.md` |
| **commands/full-review.md** | ➜ Lancer avant chaque release majeure pour valider l'ensemble du code, l'UI, et les performances | `comprehensive-review/commands/full-review.md` |

---

### CONTEXT-MANAGEMENT

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/context-manager.md** | ➜ Utiliser pour maintenir le contexte des sessions utilisateur (historique, locks, préférences) sans perte | `context-management/agents/context-manager.md` |
| **commands/context-save.md** | ➜ Déclencher pour sauvegarder l'état de la session (BPM, métronome, patterns, accords verrouillés) dans `localStorage` | `context-management/commands/context-save.md` |
| **commands/context-restore.md** | ➜ Utiliser pour restaurer une session précédente au chargement de la page | `context-management/commands/context-restore.md` |

---

### DEBUGGING-TOOLKIT

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/debugger.md** | ➜ Déclencher à chaque bug audio (Web Audio API), décalage rythmique, ou problème de rendu DOM | `debugging-toolkit/agents/debugger.md` |
| **commands/smart-debug.md** | ➜ Utiliser pour diagnostiquer les problèmes complexes (scheduler audio, synchronisation, transitions d'accords) | `debugging-toolkit/commands/smart-debug.md` |
| **agents/dx-optimizer.md** | ➜ Utiliser pour améliorer l'expérience développeur (raccourcis clavier, feedback visuel, messages d'erreur) | `debugging-toolkit/agents/dx-optimizer.md` |

---

### DOCUMENTATION-GENERATION

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/mermaid-expert.md** | ➜ Utiliser pour générer des diagrammes d'architecture (flux de la musique, structure du séquenceur, cycle de vie du scheduler) | `documentation-generation/agents/mermaid-expert.md` |
| **agents/reference-builder.md** | ➜ Utiliser pour maintenir la documentation des fonctions musicales (accords, gammes, contraintes, défis) | `documentation-generation/agents/reference-builder.md` |
| **skills/architecture-decision-records/SKILL.md** | ➜ Utiliser pour documenter les décisions techniques importantes (ex: pourquoi Web Audio API, pourquoi pas de framework) | `documentation-generation/skills/architecture-decision-records/SKILL.md` |
| **skills/changelog-automation/SKILL.md** | ➜ Utiliser pour générer automatiquement le CHANGELOG entre les versions (V17 → V18) | `documentation-generation/skills/changelog-automation/SKILL.md` |

---

### ERROR-DEBUGGING

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/debugger.md** | ➜ Déclencher pour toute erreur JavaScript non capturée, surtout dans le scheduler ou le rendu DOM | `error-debugging/agents/debugger.md` |
| **agents/error-detective.md** | ➜ Utiliser pour les erreurs intermittentes ou difficilement reproductibles (décalage rythmique, problème de timing audio) | `error-debugging/agents/error-detective.md` |
| **commands/error-analysis.md** | ➜ Utiliser pour analyser les erreurs dans la console ou les comportements inattendus dans le séquenceur | `error-debugging/commands/error-analysis.md` |
| **commands/error-trace.md** | ➜ Utiliser pour tracer la propagation d'une erreur dans le code (ex: du clic sur une case au changement de pattern) | `error-debugging/commands/error-trace.md` |

---

### FRONTEND-MOBILE-DEVELOPMENT

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/frontend-developer.md** | ➜ Déclencher pour tout développement UI, surtout responsive et tactile (séquenceur, piano, contrôles) | `frontend-mobile-development/agents/frontend-developer.md` |
| **agents/mobile-developer.md** | ➜ Utiliser pour les adaptations spécifiques mobiles (touch events, viewport, reflow, gestes tactiles) | `frontend-mobile-development/agents/mobile-developer.md` |
| **commands/component-scaffold.md** | ➜ Utiliser pour créer de nouveaux composants UI réutilisables (ex: un nouveau type de contrôle rythmique) | `frontend-mobile-development/commands/component-scaffold.md` |
| **skills/tailwind-design-system/SKILL.md** | ➜ Utiliser pour maintenir la cohérence du design system (couleurs, espacements, typographie) | `frontend-mobile-development/skills/tailwind-design-system/SKILL.md` |
| **skills/react-state-management/SKILL.md** | ➜ Adapté au pattern de gestion d'état de MuseJam (state global, re-rendu contrôlé) | `frontend-mobile-development/skills/react-state-management/SKILL.md` |

---

### FRONTEND-MOBILE-SECURITY

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/frontend-developer.md** | ➜ Utiliser pour valider la sécurité du code (pas de XSS dans les templates dynamiques, pas d'injection dans les noms d'accords) | `frontend-mobile-security/agents/frontend-developer.md` |
| **agents/frontend-security-coder.md** | ➜ Utiliser pour valider les pratiques de sécurité frontend (CSP, sanitization des entrées utilisateur) | `frontend-mobile-security/agents/frontend-security-coder.md` |
| **commands/xss-scan.md** | ➜ Lancer après l'ajout d'une nouvelle UI interactive (pickers d'accords, sélecteurs) pour vérifier l'absence de XSS | `frontend-mobile-security/commands/xss-scan.md` |

---

### GIT-PR-WORKFLOWS

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/code-reviewer.md** | ➜ Utiliser pour les revues de code avant chaque merge de feature branch | `git-pr-workflows/agents/code-reviewer.md` |
| **commands/pr-enhance.md** | ➜ Utiliser pour améliorer automatiquement les PR (formatage, messages de commit, tests manquants) | `git-pr-workflows/commands/pr-enhance.md` |
| **commands/git-workflow.md** | ➜ Utiliser pour gérer les workflows Git (branches, tags de version, commits) | `git-pr-workflows/commands/git-workflow.md` |

---

### JAVASCRIPT-TYPESCRIPT

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/javascript-pro.md** | ➜ Utiliser pour tout développement JavaScript, validation des bonnes pratiques ES6+, gestion du DOM | `javascript-typescript/agents/javascript-pro.md` |
| **skills/javascript-testing-patterns/SKILL.md** | ➜ Utiliser pour maintenir des tests (manuels ou automatisés) pour le séquenceur, le scheduler, et le générateur de patterns | `javascript-typescript/skills/javascript-testing-patterns/SKILL.md` |
| **skills/modern-javascript-patterns/SKILL.md** | ➜ Utiliser pour moderniser le code existant (map, filter, reduce, destructuring, modules) | `javascript-typescript/skills/modern-javascript-patterns/SKILL.md` |

---

### OBSERVABILITY-MONITORING

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/performance-engineer.md** | ➜ Utiliser pour analyser les performances du scheduler audio et du rendu DOM | `observability-monitoring/agents/performance-engineer.md` |

---

### SECURITY-COMPLIANCE

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/security-auditor.md** | ➜ Utiliser pour valider la sécurité du code (CSP, XSS, injections, stockage local sécurisé) | `security-compliance/agents/security-auditor.md` |
| **commands/compliance-check.md** | ➜ Lancer pour vérifier la conformité RGPD (stockage des préférences, données utilisateur) | `security-compliance/commands/compliance-check.md` |

---

### TDD-WORKFLOWS

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/tdd-orchestrator.md** | ➜ Utiliser pour structurer le développement des nouvelles fonctionnalités (Red → Green → Refactor) | `tdd-workflows/agents/tdd-orchestrator.md` |
| **commands/tdd-cycle.md** | ➜ Déclencher pour exécuter un cycle TDD complet lors de l'ajout d'une nouvelle fonctionnalité (ex: nouveau type de contrainte) | `tdd-workflows/commands/tdd-cycle.md` |
| **commands/tdd-red.md** | ➜ Utiliser pour écrire les tests avant l'implémentation (cas d'usage : génération de progression, calcul du nombre de temps) | `tdd-workflows/commands/tdd-red.md` |
| **commands/tdd-green.md** | ➜ Utiliser pour implémenter la fonctionnalité et passer les tests | `tdd-workflows/commands/tdd-green.md` |
| **commands/tdd-refactor.md** | ➜ Utiliser après validation des tests pour refactorer le code | `tdd-workflows/commands/tdd-refactor.md` |

---

### TEAM-COLLABORATION

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **commands/issue.md** | ➜ Utiliser pour créer des tickets de suivi (bugs, features, améliorations) lors du développement | `team-collaboration/commands/issue.md` |
| **commands/standup-notes.md** | ➜ Utiliser pour générer un résumé des avancées pour les daily meetings | `team-collaboration/commands/standup-notes.md` |

---

### UI-DESIGN

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/accessibility-expert.md** | ➜ Utiliser pour valider l'accessibilité des composants UI (contraste, taille des cibles tactiles, navigation) | `ui-design/agents/accessibility-expert.md` |
| **agents/design-system-architect.md** | ➜ Utiliser pour maintenir la cohérence du design system (couleurs, typographie, espacements, thème sombre) | `ui-design/agents/design-system-architect.md` |
| **agents/ui-designer.md** | ➜ Déclencher pour toute création ou modification UI (nouveaux composants, animations, responsive) | `ui-design/agents/ui-designer.md` |
| **commands/accessibility-audit.md** | ➜ Utiliser pour un audit complet de l'accessibilité de l'interface (contraste, focus, navigation clavier) | `ui-design/commands/accessibility-audit.md` |
| **commands/design-review.md** | ➜ Lancer avant chaque release majeure pour valider la cohérence visuelle de l'interface | `ui-design/commands/design-review.md` |
| **commands/create-component.md** | ➜ Utiliser pour créer de nouveaux composants UI (ex: nouvelle visualisation du piano, nouveau contrôle) | `ui-design/commands/create-component.md` |
| **skills/design-system-patterns/SKILL.md** | ➜ Utiliser pour maintenir la cohérence des composants UI (boutons, sélecteurs, cards) | `ui-design/skills/design-system-patterns/SKILL.md` |
| **skills/interaction-design/SKILL.md** | ➜ Utiliser pour concevoir les interactions (feedback visuel, animations, transitions) | `ui-design/skills/interaction-design/SKILL.md` |
| **skills/responsive-design/SKILL.md** | ➜ Utiliser pour valider et améliorer le responsive (mobile, tablette, desktop) | `ui-design/skills/responsive-design/SKILL.md` |
| **skills/visual-design-foundations/SKILL.md** | ➜ Utiliser pour les fondamentaux du design (couleurs, typographie, espacements, thème) | `ui-design/skills/visual-design-foundations/SKILL.md` |
| **skills/web-component-design/SKILL.md** | ➜ Utiliser pour concevoir des composants UI réutilisables et modulables | `ui-design/skills/web-component-design/SKILL.md` |

---

### UNIT-TESTING

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **agents/debugger.md** | ➜ Utiliser pour déboguer les tests qui échouent (génération de patterns, calcul du total des temps) | `unit-testing/agents/debugger.md` |
| **agents/test-automator.md** | ➜ Utiliser pour automatiser les tests (génération de progressions, validation des patterns) | `unit-testing/agents/test-automator.md` |
| **commands/test-generate.md** | ➜ Utiliser pour générer des tests unitaires pour les fonctions clés (générateur de progression, pattern to label) | `unit-testing/commands/test-generate.md` |

---

### CODE-DOCUMENTATION (complément)

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **skills/hads/SKILL.md** | ➜ Utiliser comme référence pour les standards de documentation interne (HADS) | `documentation-standards/skills/hads/SKILL.md` |

---

### MUSIQUE / DATA (plugins contextuels)

| Plugin | Règle de déclenchement locale | Chemin |
|:---|:---|:---|
| **business-analytics/agents/business-analyst.md** | ➜ Utiliser pour analyser les métriques d'usage (si intégration d'analytics) | `business-analytics/agents/business-analyst.md` |
| **business-analytics/skills/kpi-dashboard-design/SKILL.md** | ➜ Utiliser pour concevoir un tableau de bord de suivi (BPM, mesures jouées, patterns utilisés) | `business-analytics/skills/kpi-dashboard-design/SKILL.md` |

---

## 🚫 Plugins explicitement exclus

| Type | Raison |
|:---|:---|
| **Base de données** | Pas de SGBD, tout est en mémoire (localStorage optionnel) |
| **Backend / Frameworks** | Projet 100% frontend, pas de Django, FastAPI, Next.js, .NET, Java, Go, Rust, PHP, Ruby |
| **Cloud / Infrastructure** | Pas de déploiement conteneurisé (Terraform, Kubernetes, CI/CD, Service Mesh, Docker) |
| **Blockchain, GameDev, Data Engineering, ML, Quant, Reverse Engineering** | Hors domaine fonctionnel |
| **SEO, Marketing, RH, Légal, Ventes** | Application musicale gratuite, pas de site commercial |
| **Langages absents** | JVM, Julia, Elixir, Haskell, Shell, Bash |
| **Orchestration d'agents** | Plugin-eval, Conductor, Ship-Mate, Agent-teams — pas adapté à la taille du projet |
| **API Documentation** | `api-documenter` et `doc-generate.md` — sur une SPA Vanilla JS légère, préférer du code auto-documenté (fonctions nommées explicitement, `state.js` limpide) plutôt que de générer des blocs de commentaires superflus |
| **Performance Testing** | Pas de tests de charge nécessaires |
| **Payment Processing** | Pas de système de paiement |
| **Social Publishing** | Pas de publication sur les réseaux sociaux |

---

## 📁 Structure suggérée du projet

```
musejam/
├── index.html                 # Fichier principal (SPA)
├── assets/
│   ├── fonts/                # Polices (JetBrains Mono, Syne)
│   └── icons/                # Icônes SVG
├── docs/
│   ├── ADR/                  # Architecture Decision Records
│   └── CHANGELOG.md
├── tests/
│   └── unit/                 # Tests unitaires (fonctions musicales)
└── .github/
    └── workflows/            # GitHub Actions (validation, lint)
```

---

## 🔧 Règles d'utilisation des plugins

1. **Déclencher au bon moment** : Chaque plugin a une règle de déclenchement locale spécifique. Consulter la colonne "Règle de déclenchement locale" pour savoir quand l'utiliser.

2. **Priorité** : Toujours commencer par `debugging-toolkit` en cas de bug, `ui-design` pour le visuel, `frontend-mobile-development` pour les interactions.

3. **Documentation** : Utiliser `code-documentation` pour commenter le code, mais privilégier le code auto-documenté (fonctions nommées explicitement, variables claires).

4. **Accessibilité** : Toujours valider l'accessibilité après chaque modification UI majeure.

5. **Tests** : Suivre le cycle TDD pour les nouvelles fonctionnalités (Red → Green → Refactor).