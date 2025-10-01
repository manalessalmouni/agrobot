# 🌱 AGROBOT – Prédiction des 3 meilleures cultures

AGROBOT est une application web intelligente qui recommande les **3 cultures agricoles les plus adaptées** à votre sol et climat.  
Elle combine **Machine Learning** et **connaissances agronomiques** pour fournir des résultats personnalisés, avec conseils et alertes.

---

## 🚀 Fonctionnalités

- 🔮 **Prédiction ML** : basé sur les paramètres sol & climat (N, P, K, température, humidité, pH, pluviométrie).  
- 🌍 **Géolocalisation automatique** : pré-remplit les coordonnées GPS.  
- 📅 **Saisonnalité** : prend en compte la période de semis.  
- 💧 **Disponibilité d’irrigation** : influence la recommandation.  
- 🏪 **Préférence marché** : fruits, légumineuses, céréales, cultures de rente…  
- 🔁 **Historique de rotation** : évite de proposer la même famille botanique.  
- 📢 **Alertes maladies/parasites** spécifiques aux cultures.  
- 🌱 **Conseils d’amélioration du sol** (pH, N, P, K, eau).  
- 🌐 **Multilingue** : Français, English, Darija (RTL support).  
- 📄 **Export PDF** des résultats.  

---
## 🧠 Comment ça marche ?

1. L’utilisateur saisit les paramètres du sol (N, P, K, température, humidité, pH, pluviométrie).  
2. Les données sont passées au modèle ML (`model.pkl`), entraîné sur deux datasets ).  
3. Le modèle calcule la **probabilité d’adaptation** de chaque culture.  
4. Des **règles agronomiques** ajustent ces scores :
   - Boost si correspondance avec les préférences marché  
   - Pénalité si même famille botanique que la culture précédente  
5. Le système retourne le **Top 3 cultures** avec :
   - Image  
   - Score de confiance  
   - Groupe (fruit, légumineuse, céréale, etc.)  
   - Maladies/parasites fréquents  
   - Conseils agronomiques personnalisés  
