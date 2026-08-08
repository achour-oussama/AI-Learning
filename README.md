Charger et regarder les données
df = pd.read_csv('train.csv'). Puis df.head(), df.shape, df.columns pour voir combien de lignes/colonnes et leurs noms (Survived, Pclass, Sex, Age, Fare, etc.).
2
Diagnostic des données manquantes
df.info() puis df.isnull().sum(). Tu vas trouver des trous dans Age, Cabin et Embarked — note lesquelles et combien.
3
Stats descriptives par groupe
df['Survived'].value_counts() puis df.groupby('Sex')['Survived'].mean() et df.groupby('Pclass')['Survived'].mean(). Ça te fait pratiquer groupby tout en découvrant que le sexe et la classe influencent fortement la survie.
4
Nettoyer les colonnes
Remplis Age avec la médiane (df['Age'].fillna(df['Age'].median())), remplis Embarked avec le mode, et supprime Cabin (trop de trous) avec df.drop(columns=['Cabin']).
5
Encoder les variables catégorielles
Sex et Embarked sont du texte, Scikit-Learn veut des nombres. Utilise pd.get_dummies(df, columns=['Sex','Embarked']) ou un LabelEncoder.
6
Visualiser 2-3 relations
Avec seaborn : sns.barplot(x='Pclass', y='Survived', data=df) et sns.histplot(df['Age']). Juste pour voir visuellement ce que tu as trouvé en étape 3.
7
Split train/test
from sklearn.model_selection import train_test_split. Sépare tes features (X) de la cible (y=Survived), puis X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2).
8
Entraîner un premier modèle
from sklearn.linear_model import LogisticRegression. model.fit(X_train, y_train), puis model.predict(X_test). Compare avec y_test.