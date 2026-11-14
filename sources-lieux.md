# Où trouver les événements de chaque lieu

Ce fichier sert à la veille hebdomadaire de Sorties Paris. Chaque lieu a sa clé (entre accents graves), qu'on utilise dans le champ `v` des événements. Pour une suggestion acceptée, la clé est `s-` suivi de son identifiant.

Mention « (à confirmer) » : la page n'a pas encore été vérifiée. La veille la corrige si elle ne marche pas et met à jour la date de vérification.

## Méthode de la veille

1. Ouvrir la page « Agenda » du lieu. Si elle ne se charge pas, essayer « Aussi ».
2. En secours, chercher sur le web : `<nom du lieu> agenda <mois> <année>`. Les pages paris.fr/evenements, 75.agendaculturel.fr, unidivers.fr et agenda.parisjetaime.com donnent souvent la date, l'heure et le prix.
3. Ne garder que ce qui a lieu dans Paris intra-muros. Les conférences doivent rester accessibles, pas trop techniques (modèle : les Lundis Philo de Charles Pépin).
4. Noter les vrais horaires. Pour un cycle ou une pièce, noter les jours de la semaine et leurs heures (champ `sched`). Pour un marché, un festival ou une expo ouvert tous les jours, mettre `"daily":true`, ou un `sched` avec les horaires. Si les jours ne sont pas connus, ne mettre ni `sched` ni `daily` : l'événement va dans « Dates inconnues » et n'est rattaché à aucune date. Si la date annoncée n'est pas certaine, ajouter `"tbc":true` : l'événement va dans « Dates inconnues ou à confirmer ». Ce qui est ouvert tous les jours ou presque (au moins 5 jours par semaine) s'affiche dans la section « Tous les jours ».
5. Marquer `"outdoor":true` ce qui se passe en plein air (marchés, illuminations, balades guidées, fêtes de quartier, expositions en extérieur…). Les jours de beau temps, l'appli met ces sorties en avant ; en chercher activement, surtout parmi les événements exceptionnels.
6. Indiquer l'état des places quand la billetterie l'affiche, et retirer ce qui est complet.
7. Chaque semaine, revérifier les événements à venir déjà dans l'agenda : places, horaire, prix, annulation. Les corrections vont dans `weekly-data.patch`, sous la clé `"AAAA-MM-JJ|Titre exact"`, par exemple {"st":"ok"}, {"t":"19:00","end":"20:30"}, {"price":"12 €"}, {"st":"complet"} (l'événement disparaît) ou {"cancel":true}. Les clés des événements passés sont supprimées.

## Sources transversales

- Que faire à Paris, week-end : https://www.paris.fr/quefaire/week-end
- Que faire à Paris, recherche par lieu : https://www.paris.fr/evenements (chercher le nom du lieu)
- Agenda culturel Paris : https://75.agendaculturel.fr/ (une page par lieu)
- Paris je t'aime : https://agenda.parisjetaime.com/
- Unidivers : https://unidivers.fr/ (horaires détaillés)

## MK2 Institut — `mk2odeon` `mk2bib` `mk2bastille` `mk2gambetta` `mk2loire` `mk2nation`

- Agenda : https://www.mk2.com/evenements-en-avant/evenements-mk2-institut
- Aussi : https://www.mk2.com/evenements/cycles-de-conferences
- Astuce : la page d'un cycle liste ses séances par salle. La clé du lieu dépend de la salle (Odéon, Bibliothèque, Bastille, Gambetta, Quai de Loire, Nation). Les Lundis Philo sont à l'Odéon.

## Théâtre de la Concorde — `concorde`

- Agenda : https://theatredelaconcorde.paris/programmation/scenes-ouvertes/
- Billetterie : https://billetterie.theatredelaconcorde.paris/list/events
- Aussi : l'article paris.fr « la thématique de [mois] au Théâtre de la Concorde » (un par mois), par exemple https://www.paris.fr/evenements/la-confiance-la-thematique-de-novembre-au-theatre-de-la-concorde-126381
- Astuce : la billetterie et les pages paris.fr de chaque rencontre donnent l'heure exacte.

## Institut du monde arabe — `ima`

- Agenda : https://www.imarabe.org/fr/agenda (à confirmer)
- Billetterie : https://billetterie.imarabe.org/list/events
- Astuce : cycle Falsafa (philosophie arabe), Jeudis de l'IMA.

## Académie du Climat — `climat`

- Agenda : https://www.academieduclimat.paris/
- Aussi : https://www.paris.fr/lieux/academie-du-climat-19860

## Sciences Po — `scpo`

- Agenda : https://www.sciencespo.fr/fr/evenements/ (à confirmer)

## La Bellevilloise — `belle`

- Agenda : https://www.labellevilloise.com/ (à confirmer)
- Aussi : https://www.paris.fr/evenements (chercher « Bellevilloise »)

## Collège de France — `cdf`

- Agenda : https://www.college-de-france.fr/fr/agenda
- Aussi : « Les grands rendez-vous de [mois] » sur https://www.college-de-france.fr/fr/actualites
- Astuce : c'est gratuit et sans inscription, il faut venir 30 minutes avant. Ne garder que les grands événements et colloques grand public, pas les cours spécialisés.

## BnF – Le Collège à la Bibliothèque — `bnf`

- Agenda : https://www.bnf.fr/fr/agenda

## Maison de l'Amérique latine — `mal`

- Agenda : https://www.mal217.org/fr/agenda

## ENS Ulm — `ens`

- Agenda : https://www.ens.psl.eu/agenda

## Gaîté Lyrique — `gaite`

- Agenda : https://www.gaite-lyrique.net/agenda

## IRIS – Pascal Boniface — `iris`

- Agenda : https://www.iris-france.org/evenements/

## Philosophie Magazine — `philomag`

- Agenda : https://www.philomag.com/ (rubrique événements, à confirmer)

## Maison de la Poésie — `poesie`

- Agenda : https://www.maisondelapoesieparis.com/

## Institut d'études avancées — `iea`

- Agenda : https://www.paris-iea.fr/fr/evenements

## Le Grand Continent — `gc`

- Agenda : https://legrandcontinent.eu/fr/evenements/debats
- Aussi : https://www.billetweb.fr/ (chercher « Grand Continent »)

## Maison Heinrich Heine — `heine`

- Agenda : https://www.maison-heinrich-heine.org/ (à confirmer)

## Maison de la Chimie — `chimie`

- Astuce : la salle accueille des colloques d'autres organisateurs. Chercher « Maison de la Chimie conférence grand public ».

## Péniche Nanna — `nanna`

- Astuce : chercher « Studio Descartes anti-conférence » sur paris.fr.

## Le Consulat Voltaire (tiers-lieu) — `consulat`

- Agenda : https://leconsulat.org/agenda/

## Librairie de Paris — `libparis`

- Agenda : https://www.librairie-de-paris.fr/ (le site bloque parfois la lecture)
- Aussi : https://www.parislibrairies.fr/agenda.php (filtrer sur Librairie de Paris)

## Presse

### Le Monde — `lemonde` (35 € maximum)

- Agenda : https://ateliers.lemonde.fr/
- Aussi : chercher « Le Monde Festival » et « soirée Le Monde » avec le mois.
- Festivals du groupe : le Festival du Monde (septembre), et les festivals de M, le magazine du Monde, sur des sous-domaines dédiés (par exemple https://festival15ansdem.lemonde.fr/, site qui bloque la lecture automatique ; passer par Time Out ou paris.fr). Chercher aussi « festival M le magazine du Monde » et « Le Monde au Grand Rex ».

### Libération — `libe`

- Agenda : https://www.liberation.fr/evenements/ (à confirmer)
- Aussi : « Université Libé » sur https://www.pantheonsorbonne.fr/

### Courrier international — `courrier`

- Agenda : https://www.courrierinternational.com/ (rubrique événements)

### Le 1 hebdo – Les Lundis du 1 — `le1`

- Agenda : https://le1hebdo.fr/

### Télérama — `telerama`

- Agenda : https://www.telerama.fr/ (rubrique « Télérama Dialogues »)

## Lieux des suggestions acceptées

### Fondation Jean-Jaurès — `s-jaures`

- Agenda : https://www.jean-jaures.org/evenements
- Astuce : l'heure n'est donnée que sur la page de chaque événement (souvent 18h30–20h30).

### Collège des Bernardins — `s-bernardins`

- Agenda : https://www.collegedesbernardins.fr/agenda
- Astuce : garder les grandes soirées-débats (souvent 19h30), pas les cours de théologie.

### Mémorial de la Shoah — `s-memorial`

- Agenda : https://www.memorialdelashoah.org/ (« programme » de la période en cours)
- Aussi : https://www.paris.fr/evenements (chercher « Mémorial de la Shoah »). Les pages paris.fr donnent l'heure et le prix.

### Théâtre de la Porte Saint-Martin — `s-portestmartin`

- Agenda : https://www.portestmartin.com/
- Billetterie : https://billetterie.portestmartin.fr/

### Le Lucernaire — `s-lucernaire`

- Agenda : https://www.lucernaire.fr/
- Aussi : https://www.paris.fr/evenements (chercher « Grand entretien Lucernaire »)

### Les Plateaux Sauvages — `s-plateaux`

- Agenda : https://www.lesplateauxsauvages.fr/ (à confirmer)

### Le Carreau du Temple — `s-carreau`

- Agenda : https://www.lecarreaudutemple.eu/
- Aussi : https://75.agendaculturel.fr/le-carreau-du-temple
- Astuce : cycle de rencontres de Salomé Saqué.

### La Maison des Canaux — `s-canaux`

- Agenda : https://lamaisondescanaux.fr/ (à confirmer)
- Aussi : https://www.sortiraparis.com/en/lieux/82888-house-of-canals

## Festivals — type `fest`

Un festival se traite comme un lieu : on ne l'ajoute jamais directement à l'agenda, on le **propose** dans l'onglet Lieux. La veille l'écrit dans `weekly-data.sugs` sous la forme {"id","why","venue":{"name","arr","addr","url","about","kind":"festival"},"events":[…avec "type":"fest"]}. Il n'apparaît dans l'agenda qu'une fois accepté (clé `s-<id>`). On ne repropose pas un festival refusé (rejectedSugs). La même règle vaut pour un nouveau lieu qui n'est pas encore suivi (sans "kind":"festival").

- Agenda culturel, festivals du mois : https://75.agendaculturel.fr/festival/
- Gaîté Lyrique, festivals : https://www.gaite-lyrique.net/agenda/festival/
- Ville de Paris, « Les petits bonheurs parisiens de [mois] » : https://www.paris.fr/pages/les-petits-bonheurs-parisiens-de-novembre-25228
- Sortiraparis, « Que faire en [mois] à Paris » et le guide du week-end
- Time Out Paris, actualités : https://www.timeout.fr/paris/actualites
- Astuce : garder les festivals d'idées, de littérature, de cinéma avec débats et de journalisme. Les festivals de musique seule vont dans « Concerts », un type désactivé.

## Quand un lieu est ajouté

Si une nouvelle suggestion est acceptée ou si un lieu est ajouté dans l'appli, lui ajouter ici une section avec sa clé, la page de son agenda et une astuce.
