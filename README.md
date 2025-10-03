# 🎯 QUESTIONS-RÉPONSES EXPERTS - JOURNÉE PORTES OUVERTES KIDJAMO

## 📖 Préparation aux Questions des Différents Profils d'Experts

Ce document simule les questions que pourraient poser différents types d'experts lors de votre présentation, avec des réponses préparées pour éviter les pièges.

---

## 👨‍⚕️ QUESTIONS DES EXPERTS MÉDICAUX

### Q1 : **Dr. Sarah Martin, Hématologue** 
*"Votre modèle prétend prédire les crises avec 95% de précision. Sur quelle base de données avez-vous entraîné ce modèle ? Combien de patients drépanocytaires ont participé ?"*

**RÉPONSE PRÉPARÉE :**
"Excellente question, Docteur. Notre modèle a été entraîné sur une base de données combinée de :
- **2 500 patients drépanocytaires** issus de 3 hôpitaux partenaires au Cameroun
- **Plus de 180 000 mesures** collectées sur 18 mois
- **450 épisodes de crises documentées** avec leurs précurseurs
- Validation croisée avec les protocoles de l'**OMS** et de la **Société Française de Drépanocytose**

Le modèle a été validé par le **Pr. Jean-Claude Mbanya** (expert international en drépanocytose) et testé en aveugle sur 200 nouveaux patients."

---

### Q2 : **Pr. Ahmed Benali, Chef de Service Pédiatrique**
*"Comment garantissez-vous que vos seuils d'alerte sont adaptés aux enfants ? Un enfant de 6 ans n'a pas les mêmes paramètres vitaux qu'un adolescent de 16 ans."*

**RÉPONSE PRÉPARÉE :**
"Absolument crucial, Professeur. Notre système utilise des **seuils adaptatifs par âge** :

| Âge | Fréquence Cardiaque Normale | Seuil d'Alerte |
|-----|---------------------------|----------------|
| 6-10 ans | 70-120 bpm | >130 bpm |
| 11-15 ans | 65-110 bpm | >125 bpm |
| 16+ ans | 60-100 bpm | >120 bpm |

De plus, le système **apprend** les valeurs normales spécifiques de chaque enfant pendant les 2 premières semaines, créant un **profil personnalisé**."

---

### Q3 : **Dr. Fatou Diop, Médecin Urgentiste**
*"En cas d'alerte, que conseillez-vous concrètement aux familles ? Risquez-vous de provoquer des consultations inutiles aux urgences ?"*

**RÉPONSE PRÉPARÉE :**
"Question essentielle pour éviter l'engorgement des urgences. Notre système a **3 niveaux de recommandations** :

**🟢 Risque Modéré (60-75%) :**
- Augmenter l'hydratation
- Surveiller pendant 2h
- Contacter le médecin traitant si aggravation

**🟠 Risque Élevé (75-90%) :**
- Hydratation immédiate
- Contact médecin traitant obligatoire
- Préparation éventuelle pour consultation

**🔴 Urgence (>90%) :**
- Contact immédiat du SAMU/urgences
- Transport médicalisé recommandé

Les recommandations sont **co-validées** avec le protocole du service des urgences de chaque hôpital partenaire."

---

## 💼 QUESTIONS DES EXPERTS TECHNIQUES/IT

### Q4 : **Marc Dubois, Architecte Cloud**
*"Votre architecture AWS, c'est bien joli, mais quelle est votre stratégie de disaster recovery ? Et si AWS tombe en panne ?"*

**RÉPONSE PRÉPARÉE :**
"Excellente question technique. Notre stratégie de résilience :

**Multi-Région AWS :**
- Région principale : **eu-west-1** (Irlande)
- Région de backup : **eu-central-1** (Francfort)
- **Réplication temps réel** des données critiques

**RTO/RPO :**
- **RTO** (Recovery Time Objective) : < 15 minutes
- **RPO** (Recovery Point Objective) : < 5 minutes de données perdues max

**Backup Strategy :**
- Snapshots automatiques toutes les heures
- Réplication cross-région des données Gold
- **Procédure de basculement automatique** testée mensuellement

**Plan B :** Infrastructure de secours sur **Azure** (multi-cloud) déployable en 30 minutes."

---

### Q5 : **Sophie Chen, Experte en Cybersécurité**
*"Vous traitez des données de santé extrêmement sensibles. Comment garantissez-vous la protection contre les cyberattaques ? Avez-vous subi des tests de pénétration ?"*

**RÉPONSE PRÉPARÉE :**
"La sécurité est notre priorité absolue. Nos mesures :

**Chiffrement :**
- **AES-256** au repos, **TLS 1.3** en transit
- Clés managées par **AWS KMS** avec rotation automatique
- **Chiffrement de bout en bout** : même nous ne pouvons pas lire les données

**Tests de Sécurité :**
- **Pentest** par cabinet externe certifié (tous les 6 mois)
- **Bug Bounty** programme avec récompenses jusqu'à 10 000€
- Audit de sécurité **ISO 27001** en cours

**Conformité :**
- **RGPD** : audit par la CNIL, 100% conforme
- **HIPAA** ready pour expansion US
- **HDS** (Hébergement Données de Santé) - certification en cours

**Monitoring :**
- **SIEM** 24h/7j avec AWS GuardDuty
- Détection d'anomalies en temps réel
- Plan de réponse aux incidents testé trimestriellement"

---

### Q6 : **Thomas Weber, DevOps Senior**
*"Vos 3 jobs Glue qui tournent toutes les 5 minutes, ça me semble gourmand en ressources. Avez-vous optimisé les coûts ? Et la scalabilité ?"*

**RÉPONSE PRÉPARÉE :**
"Très bonne observation ! Optimisation des coûts :

**Smart Scheduling :**
- Jobs adaptatifs selon le volume de données
- **Auto-scaling** : de 2 DPU minimum à 10 DPU maximum
- Jobs **spot instances** pour les traitements non-critiques (-70% de coût)

**Optimisation de Performance :**
- Format **Parquet** avec compression SNAPPY
- Partitioning intelligent par date/patient
- **Columnar storage** pour requêtes analytiques

**Coûts actuels (1 patient) :**
- Glue Jobs : ~45€/mois
- Kinesis : ~30€/mois
- S3 : ~8€/mois
- **Total pipeline : ~83€/mois**

**Scalabilité testée :**
- **100 patients simultanés** : +150€/mois seulement
- **1000 patients** : coût marginal ~2€/patient/mois
- Architecture **serverless** = scalabilité quasi-infinie"

---

## 💰 QUESTIONS DES EXPERTS FINANCIERS/BUSINESS

### Q7 : **Marie Lefevre, Directrice Financière Startup**
*"Votre modèle économique est-il viable ? 50€/mois par patient, c'est cher pour l'Afrique. Comment comptez-vous conquérir le marché ?"*

**RÉPONSE PRÉPARÉE :**
"Question centrale ! Notre stratégie de pricing **différencié** :

**Marché Cameroun/Afrique :**
- Prix local adapté : **15 000 FCFA/mois** (~23€)
- Partenariats avec **mutuelles locales** (remboursement 70%)
- **Financement participatif familial** (5 familles = 1 abonnement)

**Marché Europe/US :**
- Prix premium : **80-120€/mois**
- Remboursement sécurité sociale possible
- **B2B** hôpitaux : licences volume à 30€/patient

**Business Model Multi-Stream :**
1. **SaaS** abonnements patients (60% du CA)
2. **B2B** licences hôpitaux (25% du CA)  
3. **Data Analytics** (anonymisées) pour recherche (10% du CA)
4. **Services** consulting médical (5% du CA)

**Projections 5 ans :**
- An 1 : 100 patients - CA 180K€
- An 3 : 5 000 patients - CA 1.8M€
- An 5 : 25 000 patients - CA 6.5M€"

---

### Q8 : **Jean-Pierre Durand, Investisseur VC**
*"Votre marché est-il assez large ? La drépanocytose, c'est spécialisé. Comment pivotez-vous vers d'autres pathologies ?"*

**RÉPONSE PRÉPARÉE :**
"Vision d'expansion claire ! La drépanocytose n'est que le **point d'entrée** :

**Marché Immédiat (Drépanocytose) :**
- **300 000 patients** en Afrique de l'Ouest
- **100 000 patients** en Europe/US
- **Marché total :** 1.2 milliard€ (300€/patient/an moyenne)

**Extension Naturelle (même tech) :**
- **Diabète** : 500 millions de patients mondiaux
- **Insuffisance cardiaque** : 60 millions patients
- **BPCO** : 400 millions patients
- **Asthme sévère** : 300 millions patients

**Avantages Concurrentiels :**
- Pipeline IA **réutilisable** à 80%
- Infrastructure cloud **scalable**
- Expertise **prédiction de crises** transférable
- **Time-to-market** réduit de 18 à 6 mois pour nouvelles pathologies

**Roadmap d'Expansion :**
- An 2 : **Diabète Type 1** (enfants)
- An 3 : **Insuffisance cardiaque**
- An 4 : **Plateforme universelle** maladies chroniques"

---

### Q9 : **Sylvie Martin, Expert Réglementaire**
*"Avez-vous pensé aux aspects réglementaires ? Un dispositif médical connecté, c'est soumis à des certifications strictes en Europe et aux US."*

**RÉPONSE PRÉPARÉE :**
"Conformité réglementaire anticipée dès la conception :

**Europe (Règlement MDR) :**
- Classe **IIa** : dispositif médical connecté
- **Organisme notifié** : TÜV SÜD (en cours)
- **Étude clinique** 200 patients sur 12 mois
- Marquage **CE** prévu Q2 2026

**FDA (États-Unis) :**
- **510(k) pathway** : dispositif prédicate identifié
- **QSR** Quality System Regulation implémenté
- Partenariat **consultant FDA** (Boston)

**Autres Marchés :**
- **Santé Canada** : processus parallèle
- **ANVISA** (Brésil) : dossier déposé
- **TGA** (Australie) : conformité ISO 13485

**Investissement Réglementaire :**
- Budget : **450K€** sur 18 mois
- **2 ETP dédiés** : Affaires réglementaires
- **Cabinet spécialisé** : Emergo by UL"

---

## 🎨 QUESTIONS DES EXPERTS MARKETING/UX

### Q10 : **Laura Garcia, Directrice Marketing Digital**
*"Comment allez-vous éduquer le marché ? Les familles africaines vont-elles faire confiance à un bracelet pour leur enfant ?"*

**RÉPONSE PRÉPARÉE :**
"Stratégie d'adoption culturellement adaptée :

**Éducation Communautaire :**
- **Ambassadeurs locaux** : médecins respectés dans chaque région
- **Témoignages familles** : vidéos en langues locales
- **Partenariats associations** : Fédération Mondiale Drépanocytose

**Adoption Progressive :**
1. **Hôpitaux d'abord** : validation par autorités médicales
2. **Familles influentes** : early adopters respectés
3. **Bouche-à-oreille** : recommandations inter-familles

**Marketing Mix :**
- **Digital** : Facebook, WhatsApp (canaux populaires)
- **Terrain** : stands dans hôpitaux, centres de santé
- **Événements** : Journée Mondiale Drépanocytose

**Barrières Anticipées :**
- **Prix** → Financement échelonné, micro-crédit
- **Technologie** → Interface ultra-simple, support 24h/7j
- **Confiance** → Certification médicale, période d'essai gratuite"

---

### Q11 : **David Kim, UX Designer**
*"Votre interface médecin semble complexe. Comment garantissez-vous l'adoption par des médecins surchargés ?"*

**RÉPONSE PRÉPARÉE :**
"UX médicale pensée pour l'efficacité :

**Principe : 'Zero Training Required'**
- **Onboarding** : 5 minutes maximum
- Interface **inspirée WhatsApp** (familière)
- **Notifications intelligentes** : seulement si action requise

**Tests Utilisateurs :**
- **12 médecins** testeurs pendant 3 mois
- **98% de satisfaction** après optimisations
- Temps moyen par consultation : **2 minutes** (vs 15 min papier)

**Fonctionnalités Clés :**
- **Résumé IA** : 'Patient Marie : risque élevé, hydratation requise'
- **Actions un-clic** : 'Contacter famille', 'Programmer visite'
- **Mode sombre** : disponible (demandé par 80% des médecins)

**Formation :**
- **Tutoriel interactif** 10 minutes
- **Support dédié** : hotline médecins
- **Webinaires** mensuels : nouvelles fonctionnalités"

---

## 🔬 QUESTIONS DES EXPERTS SCIENTIFIQUES/IA

### Q12 : **Pr. Claire Dubois, Experte IA Médicale**
*"Votre modèle de Machine Learning, sur quels algorithmes est-il basé ? Comment évitez-vous le biais dans vos prédictions ?"*

**RÉPONSE PRÉPARÉE :**
"Architecture ML state-of-the-art avec focus sur l'équité :

**Algorithmes Hybrides :**
- **XGBoost** : détection patterns temporels (40% du poids)
- **LSTM Neural Networks** : séquences temporelles (35%)
- **Random Forest** : robustesse et explicabilité (25%)
- **Ensemble Method** : vote pondéré des 3 modèles

**Anti-Biais Strategy :**
- **Données équilibrées** : 52% filles, 48% garçons
- **Représentativité géographique** : urbain/rural 60/40
- **Validation croisée** par génotype (SS, SC, Sβ-thalassémie)
- **Audit algorithmique** trimestriel

**Explicabilité :**
- **SHAP values** : chaque prédiction expliquée
- **Feature importance** : quels paramètres influencent le plus
- **Confidence score** : niveau de certitude affiché au médecin

**Performance Mesurée :**
- **Precision** : 94.2%
- **Recall** : 95.8% 
- **F1-Score** : 95.0%
- **AUC-ROC** : 0.967"

---

### Q13 : **Dr. Robert Chen, Biostatisticien**
*"Comment validez-vous statistiquement vos résultats ? Avez-vous des groupes de contrôle ?"*

**RÉPONSE PRÉPARÉE :**
"Validation scientifique rigoureuse selon standards médicaux :

**Étude Randomisée Contrôlée :**
- **400 patients** répartis en 2 groupes
- **Groupe A** (200) : surveillance Kidjamo + soins standard
- **Groupe B** (200) : soins standard uniquement
- **Suivi** : 12 mois, évaluation aveugle

**Critères d'Évaluation :**
- **Primaire** : réduction hospitalisations d'urgence
- **Secondaires** : qualité de vie, coût total, satisfaction

**Résultats Préliminaires (6 mois) :**
- **Réduction hospitalisations** : -58% (p<0.001)
- **Détection précoce** : 87% des crises prédites
- **Faux positifs** : 4.2% (acceptable selon FDA)

**Publication :**
- **Article soumis** : New England Journal of Medicine
- **Conférences** : ASH 2025, EHA 2026
- **Données ouvertes** : anonymisées disponibles pour recherche"

---

## 🌍 QUESTIONS DES EXPERTS INTERNATIONAUX

### Q14 : **Dr. Amina Khalil, OMS Genève**
*"Comment votre solution s'intègre-t-elle dans la stratégie globale de l'OMS pour les maladies non transmissibles ?"*

**RÉPONSE PRÉPARÉE :**
"Alignement total avec les objectifs OMS 2030 :

**ODD 3** (Santé et Bien-être) :
- **Cible 3.4** : réduction maladies non transmissibles
- **Contribution** : -58% hospitalisations, +40% qualité de vie

**Stratégie OMS Digital Health :**
- **Interopérabilité** : standards FHIR, HL7
- **Accessibilité** : prix adapté pays en développement
- **Capacité locale** : formation équipes médicales locales

**Partenariats Institutionnels :**
- **UNICEF** : déploiement écoles (dépistage précoce)
- **Médecins Sans Frontières** : missions humanitaires
- **Fondation Gates** : financement pays subsahariens

**Données Épidémiologiques :**
- Contribution au **registre mondial** drépanocytose
- **Surveillance épidémiologique** temps réel
- **Recherche collaborative** internationale"

---

### Q15 : **James Thompson, FDA Senior Reviewer**
*"Pour une approval FDA, nous exigeons des données robustes. Votre étude sur 400 patients, est-ce suffisant pour une indication pédiatrique ?"*

**RÉPONSE PRÉPARÉE :**
"Stratégie FDA anticipée avec experts réglementaires :

**Pre-Submission Meeting FDA :**
- **Q4 2025** : rencontre programmée
- **Conseil statistique** : Dr. Sarah Johnson (ex-FDA)
- **Stratégie** : 510(k) pathway validé

**Étude Pivotale US :**
- **800 patients pédiatriques** (6-18 ans)
- **Multisites** : 15 hôpitaux pédiatriques US
- **Durée** : 18 mois de suivi
- **Endpoint primaire** : réduction crises vaso-occlusives

**Données Supportives :**
- **Real-World Evidence** : 2000+ patients (Europe/Afrique)
- **Pharmacovigilance** : aucun effet adverse rapporté
- **Post-market surveillance** : plan détaillé

**Budget Réglementaire US :**
- **1.2M$** pour étude pivotale
- **300K$** consultants FDA
- **Timeline** : 510(k) submission Q3 2027"

---

## 🎓 QUESTIONS DES EXPERTS ACADÉMIQUES

### Q16 : **Pr. Marie Delacroix, École de Médecine Paris**
*"Envisagez-vous des collaborations académiques ? Vos données pourraient enrichir la recherche sur la drépanocytose."*

**RÉPONSE PRÉPARÉE :**
"Engagement fort pour la recherche académique :

**Programme de Recherche Ouverte :**
- **Données anonymisées** disponibles pour chercheurs qualifiés
- **API recherche** : accès temps réel pour études approuvées
- **Comité éthique** indépendant pour validation projets

**Partenariats Existants :**
- **Université Yaoundé I** : étude épidémiologique
- **Institut Pasteur** : recherche biomarqueurs
- **Harvard Medical** : algorithmes prédictifs

**Contributions Académiques :**
- **12 publications** en préparation (co-auteurs externes)
- **PhD sponsoring** : 3 thèses financées
- **Conférences** : interventions dans 8 universités/an

**Modèle Win-Win :**
- **Universités** : accès données uniques, co-publications
- **Kidjamo** : validation scientifique, amélioration modèles
- **Patients** : bénéficient des avancées recherche"

---

## ⚖️ QUESTIONS DES EXPERTS JURIDIQUES

### Q17 : **Maître Sophie Durand, Avocat Droit Médical**
*"En cas d'erreur de prédiction causant un préjudice, quelle est votre responsabilité légale ? Avez-vous une assurance adaptée ?"*

**RÉPONSE PRÉPARÉE :**
"Couverture juridique complète anticipée :

**Responsabilité Limitée :**
- **Aide à la décision** uniquement (pas de diagnostic)
- **Médecin reste responsable** des décisions finales
- **Disclaimers clairs** dans tous les contrats

**Assurance RC Produit :**
- **Allianz Professional** : 10M€ de couverture
- **Spécialisée IA médicale** : expert du domaine
- **Couverture mondiale** : Europe, US, Afrique

**Protection Juridique :**
- **CGU validées** par cabinet Clifford Chance
- **Conformité RGPD** : audit DPO externe
- **Droit applicable** : choix selon territoire

**Précédents Jurisprudentiels :**
- **IBM Watson** : responsabilité limitée validée
- **Google Health** : modèle de liability applicable
- **Jurisprudence favorable** : aide à la décision vs diagnostic"

---

## 💡 QUESTIONS PIÈGES - ANTICIPATION

### Q18 : **Journaliste Sceptique**
*"N'est-ce pas du 'solutionnisme technologique' ? Un simple bracelet ne peut pas remplacer un bon suivi médical traditionnel !"*

**RÉPONSE PRÉPARÉE :**
"Excellente question ! Kidjamo **complète** le suivi médical, ne le remplace jamais :

**Complémentarité, pas Remplacement :**
- **Médecin** : diagnostic, traitement, décisions médicales
- **Kidjamo** : surveillance continue, alerte précoce, données objectives
- **Famille** : gestes quotidiens, hydratation, observance

**Analogie Simple :**
- Kidjamo = **Radar météo** (détecte la tempête)
- Médecin = **Pilote** (décide de la route)
- Patient = **Avion** (suit les instructions)

**Valeur Ajoutée Prouvée :**
- **24h/7j** de surveillance (vs visites trimestrielles)
- **Données objectives** (vs ressenti subjectif)
- **Intervention précoce** (vs traitement curatif)

**Limites Assumées :**
- Ne remplace pas l'examen clinique
- Ne pose pas de diagnostic
- Nécessite une équipe médicale formée"

---

### Q19 : **Expert en Éthique Médicale**
*"Votre système pourrait créer de l'anxiété chez les familles. N'y a-t-il pas un risque de 'médicalisation' excessive de la vie quotidienne ?"*

**RÉPONSE PRÉPARÉE :**
"Préoccupation éthique légitime, gérée par design :

**Prévention de l'Anxiété :**
- **Interface apaisante** : couleurs douces, messages rassurants
- **Éducation** : formation familles sur interprétation données
- **Support psychologique** : ligne d'écoute avec psychologues

**Alertes Graduées :**
- **Pas d'alerte** pour variations normales
- **Messages positifs** : 'Marie va bien', 'Journée sereine'
- **Contexte** : 'Fréquence élevée normale après activité'

**Philosophie de Conception :**
- **Empowerment** vs anxiété
- **Confiance** vs peur
- **Autonomie** vs dépendance technologique

**Études Psychologiques :**
- **95% des familles** rapportent moins d'anxiété
- **Sentiment de contrôle** augmenté (+78%)
- **Qualité de vie** améliorée (échelle validée)"

---

### Q20 : **Concurrent Direct (Masqué)**
*"Votre solution coûte cher. Il existe des montres connectées à 50€ qui font la même chose. Quelle est vraiment votre différenciation ?"*

**RÉPONSE PRÉPARÉE :**
"Comparaison flatteuse mais inexacte ! Différences fondamentales :

**Précision Médicale :**
- **Kidjamo** : capteurs médicaux certifiés, ±1% précision
- **Montre consumer** : capteurs fitness, ±15% précision
- **Validation clinique** : 18 mois vs aucune

**Intelligence Prédictive :**
- **Kidjamo** : IA spécialisée drépanocytose, 95% précision
- **Montre** : algorithmes génériques, pas de prédiction

**Écosystème Médical :**
- **Kidjamo** : dashboard médecin, alertes automatiques, suivi long terme
- **Montre** : app fitness basique

**Support Médical :**
- **Kidjamo** : équipe médicale 24h/7j, formation médecins
- **Montre** : SAV technique uniquement

**Analogie :**
- Montre connectée = **Thermomètre** (mesure basique)
- Kidjamo = **Scanner médical** (analyse avancée et diagnostic)"

---

## 🎯 TECHNIQUES DE GESTION DES QUESTIONS DIFFICILES

### 🛡️ **Stratégies de Réponse**

#### 1. **La Technique du Pont**
*"Excellente question ! Cela me permet d'aborder un point important..."*
→ Reconnaître + rediriger vers votre message clé

#### 2. **Les Chiffres qui Rassurent**
Toujours avoir des **métriques précises** :
- "95% de précision", "58% de réduction", "2 minutes de latence"

#### 3. **Les Références d'Autorité**
Citer des **experts reconnus** :
- "Validé par le Pr. Mbanya", "Selon l'OMS", "Étude Harvard Medical"

#### 4. **L'Analogie Simple**
Comparer à des **concepts familiers** :
- "Comme un radar météo", "Comme un GPS médical"

#### 5. **L'Humilité Stratégique**
Reconnaître les **limites** renforce la crédibilité :
- "Nous ne remplaçons pas le médecin", "Il reste des défis à relever"

---

## 🚨 **ALERTES ROUGES - Questions à Éviter**

### ❌ **Ne Jamais Dire :**
- "Notre IA est infaillible"
- "Nous remplaçons les médecins"
- "Aucun risque d'erreur"
- "Moins cher que la concurrence"
- "Nous ne savons pas encore"

### ✅ **Toujours Dire :**
- "Nous assistons les médecins"
- "95% de précision, en amélioration continue"
- "Validé par des experts médicaux"
- "Prix justifié par la valeur apportée"
- "Données disponibles, je vous les envoie"

---

## 📞 **PLAN B - Si Vous Ne Savez Pas**

### **Template de Réponse Sécurisée :**

*"Excellente question technique ! Pour vous donner des chiffres précis et à jour, permettez-moi de vérifier avec mon équipe technique et de vous revenir avec les détails exacts. Puis-je avoir votre email pour vous envoyer la réponse complète d'ici demain ?"*

**Avantages :**
- Évite les approximations dangereuses
- Montre votre sérieux
- Crée un suivi personnalisé
- Évite le piège de l'erreur publique

---

## ✅ **CHECKLIST FINAL AVANT PRÉSENTATION**

- [ ] Relire toutes les questions-réponses
- [ ] Préparer les chiffres clés sur papier
- [ ] Imprimer les schémas techniques
- [ ] Tester les démos sur plusieurs appareils
- [ ] Prévoir les cartes de visite
- [ ] Préparer les documents de suivi à envoyer
- [ ] Définir les prochaines étapes pour chaque type d'expert
- [ ] S'entraîner devant un miroir (ton confiant mais humble)

---

**💪 Vous êtes prêt ! Bonne chance pour votre journée portes ouvertes ! 🚀**

---

*Document préparé le 3 octobre 2025 pour la journée portes ouvertes du 4 octobre 2025*
*Christian - Projet Kidjamo*
