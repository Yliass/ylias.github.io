<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AZ-900 Cheat Sheet - Fondamentaux Microsoft Azure</title>
<style>
    body {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        line-height: 1.6;
        color: #333;
        background-color: #f4f4f4;
        margin: 0;
        padding: 0;
    }

    header {
        background-color: #0078d4;
        color: white;
        text-align: center;
        padding: 2rem;
        box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }

    header h1 {
        margin: 0;
        font-size: 2.5rem;
    }

    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 1rem;
    }

    .section {
        background-color: white;
        border-radius: 8px;
        margin-bottom: 1.5rem;
        box-shadow: 0 1px 3px rgba(0,0,0,0.1);
        overflow: hidden;
    }

    .section-header {
        background-color: #0078d4;
        color: white;
        padding: 1rem;
        cursor: pointer;
        font-size: 1.5rem;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .section-header::after {
        content: '\25BC';
        font-size: 1rem;
    }

    .section-content {
        padding: 1rem;
        display: none;
    }

    .section.active .section-content {
        display: block;
    }

    .section.active .section-header::after {
        content: '\25B2';
    }

    .subsection {
        margin-bottom: 1rem;
    }

    .subsection h3 {
        color: #0078d4;
        font-size: 1.2rem;
        margin-bottom: 0.5rem;
    }

    ul {
        list-style-type: disc;
        padding-left: 1.5rem;
    }

    li {
        margin-bottom: 0.5rem;
    }

    .percentage {
        font-style: italic;
        color: #666;
    }

    footer {
        text-align: center;
        padding: 1rem;
        background-color: #0078d4;
        color: white;
        margin-top: 2rem;
    }

    @media (max-width: 768px) {
        header h1 {
            font-size: 2rem;
        }

        .section-header {
            font-size: 1.3rem;
        }
    }
</style>
</head>
<body>
<header>
    <h1>AZ-900 Cheat Sheet : Fondamentaux Microsoft Azure</h1>
    <p>Version mise à jour au 30 octobre 2025. Conçu pour vous aider à obtenir 1000/1000 !</p>
</header>

<div class="container">

    <!-- SECTION 1 -->
    <div class="section">
        <div class="section-header" onclick="toggleSection(this)">
            Concepts du Cloud (25–30%)
        </div>
        <div class="section-content">

            <div class="subsection">
                <h3>Comprendre le Cloud Computing</h3>
                <ul>
                    <li><strong>Définition</strong> : Fourniture de services informatiques (serveurs, stockage, bases de données, réseau, logiciels) via Internet, à la demande et payés à l’usage.</li>
                    <li><strong>Modèle de responsabilité partagée</strong> : Microsoft gère l’infrastructure physique, le client gère les données et les accès.</li>
                    <li><strong>Modèles de cloud</strong> : Public (ouvert à tous), Privé (dédié à une organisation), Hybride (combinaison des deux).</li>
                    <li><strong>Cas d’usage</strong> : Public pour scalabilité, Privé pour conformité, Hybride pour migration progressive.</li>
                    <li><strong>Modèle basé sur la consommation</strong> : Payer seulement pour ce qui est utilisé, sans investissement initial.</li>
                    <li><strong>Comparaison des modèles de tarification</strong> : Paiement à l’usage vs réservations (réductions pour engagements longs).</li>
                    <li><strong>Serverless</strong> : Exécution de code sans gérer les serveurs (ex : Azure Functions).</li>
                </ul>
            </div>

            <div class="subsection">
                <h3>Avantages des services Cloud</h3>
                <ul>
                    <li><strong>Haute disponibilité et scalabilité</strong> : Redondance et auto-scaling pour gérer les pics de charge.</li>
                    <li><strong>Fiabilité et prévisibilité</strong> : SLA garantis, sauvegardes automatiques.</li>
                    <li><strong>Sécurité et gouvernance</strong> : Outils intégrés pour conformité et protection.</li>
                    <li><strong>Facilité de gestion</strong> : Mises à jour automatiques, monitoring centralisé.</li>
                </ul>
            </div>

            <div class="subsection">
                <h3>Types de services Cloud</h3>
                <ul>
                    <li><strong>IaaS</strong> : Infrastructure (VMs, stockage, réseau) – contrôle maximal.</li>
                    <li><strong>PaaS</strong> : Plateforme (applications, bases de données) – focus sur le code, Azure gère l’infrastructure.</li>
                    <li><strong>SaaS</strong> : Logiciel prêt à l’emploi (ex : Office 365).</li>
                    <li><strong>Cas d’usage</strong> : IaaS pour lift-and-shift, PaaS pour développement rapide, SaaS pour productivité.</li>
                </ul>
            </div>
        </div>
    </div>

    <!-- SECTION 2 -->
    <div class="section">
        <div class="section-header" onclick="toggleSection(this)">
            Architecture et services Azure (35–40%)
        </div>
        <div class="section-content">

            <div class="subsection">
                <h3>Composants architecturaux principaux</h3>
                <ul>
                    <li><strong>Régions et paires de régions</strong> : Centres de données géographiques (ex : France Central), paires pour redondance.</li>
                    <li><strong>Zones de disponibilité</strong> : Centres de données isolés dans une région pour haute disponibilité.</li>
                    <li><strong>Ressources et groupes de ressources</strong> : Organisation logique des ressources.</li>
                    <li><strong>Abonnements</strong> : Gestion de facturation et droits d’accès.</li>
                    <li><strong>Groupes de gestion</strong> : Gestion de plusieurs abonnements avec des politiques communes.</li>
                    <li><strong>Hiérarchie</strong> : Groupes de gestion > Abonnements > Groupes de ressources > Ressources.</li>
                </ul>
            </div>

            <div class="subsection">
                <h3>Services de calcul et réseau</h3>
                <ul>
                    <li><strong>Types de calcul</strong> : Machines virtuelles, Conteneurs, Fonctions (serverless).</li>
                    <li><strong>Options pour VMs</strong> : VMs Azure, Scale Sets (auto-scale), Availability Sets (HA), Virtual Desktop.</li>
                    <li><strong>Hébergement d’applications</strong> : Web Apps (PaaS), Conteneurs (ACI/AKS), VMs (IaaS).</li>
                    <li><strong>Réseaux virtuels</strong> : VNet, Sous-réseaux, Peering, DNS, VPN Gateway, ExpressRoute.</li>
                    <li><strong>Points d’accès</strong> : Public (internet), Privé (via VNet).</li>
                </ul>
            </div>

            <div class="subsection">
                <h3>Services de stockage Azure</h3>
                <ul>
                    <li><strong>Types de stockage</strong> : Blob, Fichier, Queue, Table, Disque.</li>
                    <li><strong>Niveaux</strong> : Hot, Cool, Archive.</li>
                    <li><strong>Redondance</strong> : LRS, ZRS, GRS, RA-GRS.</li>
                    <li><strong>Outils</strong> : AzCopy, Storage Explorer, File Sync.</li>
                    <li><strong>Migration</strong> : Azure Migrate, Data Box.</li>
                </ul>
            </div>

            <div class="subsection">
                <h3>Identité, accès et sécurité</h3>
                <ul>
                    <li><strong>Microsoft Entra ID</strong> : Annuaire cloud pour gérer les identités.</li>
                    <li><strong>Méthodes d’authentification</strong> : SSO, MFA, Passwordless.</li>
                    <li><strong>Identités externes</strong> : B2B (entre entreprises), B2C (consommateurs).</li>
                    <li><strong>Accès conditionnel</strong> : Politiques basées sur le risque (localisation, appareil).</li>
                    <li><strong>RBAC</strong> : Rôles Owner, Contributor, Reader.</li>
                    <li><strong>Zero Trust</strong> : Toujours vérifier, accès minimal, présumer une faille.</li>
                    <li><strong>Defense-in-depth</strong> : Couches multiples de sécurité.</li>
                    <li><strong>Microsoft Defender pour le Cloud</strong> : Gestion de la sécurité et protection contre les menaces.</li>
                </ul>
            </div>
        </div>
    </div>

    <!-- SECTION 3 -->
    <div class="section">
        <div class="section-header" onclick="toggleSection(this)">
            Gestion et gouvernance Azure (30–35%)
        </div>
        <div class="section-content">

            <div class="subsection">
                <h3>Gestion des coûts</h3>
                <ul>
                    <li><strong>Facteurs influents</strong> : Région, bande passante, type de ressource, utilisation.</li>
                    <li><strong>Calculateur de prix</strong> : Estimer les coûts mensuels.</li>
                    <li><strong>Outils de gestion des coûts</strong> : Budgets, alertes, analyses.</li>
                    <li><strong>Tags</strong> : Catégorisation et suivi des coûts.</li>
                </ul>
            </div>

            <div class="subsection">
                <h3>Outils de gouvernance et conformité</h3>
                <ul>
                    <li><strong>Microsoft Purview</strong> : Gouvernance et conformité des données.</li>
                    <li><strong>Azure Policy</strong> : Application de règles (ex : régions autorisées).</li>
                    <li><strong>Verrous de ressources</strong> : Protection contre suppression accidentelle.</li>
                </ul>
            </div>

            <div class="subsection">
                <h3>Outils de gestion et déploiement des ressources</h3>
                <ul>
                    <li><strong>Portail Azure</strong> : Interface web pour gérer les ressources.</li>
                    <li><strong>Cloud Shell</strong> : CLI/PowerShell dans le navigateur.</li>
                    <li><strong>Azure Arc</strong> : Gestion des ressources hybrides ou locales.</li>
                    <li><strong>Infrastructure as Code (IaC)</strong> : Déploiement via code (ARM, Bicep).</li>
                </ul>
            </div>

            <div class="subsection">
                <h3>Outils de surveillance</h3>
                <ul>
                    <li><strong>Azure Advisor</strong> : Recommandations pour coûts, sécurité et performances.</li>
                    <li><strong>Azure Service Health</strong> : État des services et incidents.</li>
                    <li><strong>Azure Monitor</strong> : Metrics, logs et alertes.</li>
                </ul>
            </div>

        </div>
    </div>

</div>

<footer>
    <p>Créé par Grok — Basé sur le guide officiel Microsoft. Bonne chance pour votre examen AZ-900 !</p>
</footer>

<script>
    function toggleSection(element) {
        const section = element.parentElement;
        section.classList.toggle('active');
    }
</script>

</body>
</html>
