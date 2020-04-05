# Portfolio
## **Lesweek 2**
### *Reflectie proces*
Deze lesweek was er nog niet heel veel werk dat gedaan moest worden. De opdrachten werden dus voornamelijk in paren gedaan. Ook was het werk nu nog niet heel moeilijk of nieuw. De opdrachten waren dingen die we al geleerd hadden in de vorige perioden. Aangezien het werk niet heel moeilijk was waren we dus ook al snel klaar met het maken van deze opdrachten.
Mijn bijdrage aan de proftaak in week 2, bestond voornamelijk uit het uitschrijven van het klassendiagram die gemaakt is in week 1. Daarbij heb ik een aantal aanpassingen en naam aanpassingen gemaakt in het voorgemaakte diagram. Uiteraard heb ik dit eerst voorgestelt aan de andere projectleden, voordat ik met deze aanpassingen aan de slag ging. De reden voor deze aanpassingen was vooral omdat het klassen diagram gemaakt in lesweek 1, meer een idee was dan echt een vastgesteld plan.
Sjoerd kwam in week 1 met het voorstel om zijn framework te gaan gebruiken we vonden bijna allemaal dit een prima idee op 2 leden na. Echt een keuze hebben we nog niet gemaakt maar ben ik er wel van overtuigd dat we het waarschijnlijk gaan gebruiken. Voor de rest ging het werken zelf goed, we liepen niet tegen problemen aan en konden de dag snel afronden.

### *Reflectie vakinhoudelijk*
Het is de eerste lesweek van de proftaak waar er echt code geschreven moet worden. De eerste lesweek bestond voornamelijk op het opstellen van het plan van aanpak en jezelf orienteren op de opdracht die de volgende weken gemaakt moet worden. We hebben dus ook in week 1 een klassendiagram, die breedt het idee geeft van wat er gemaakt moet worden gemaakt.
![Klassendiagram](images/klassendiagram.jpg)
Ik had de taak gekregen om dus deze klassendiagram te brengen naar het project. Ook moest ik meteen de variabelen erbij gaan schrijven en dus gaan denken over wat wat nodig heeft. Het was nog niet heel belangrijk of dat alles precies had wat de klasse nodig had. Aangezien we de data toch wouden gaan scheiden van de simulatie klassen. Dus heb ik bij elke klasse wat variabelen erbij gedaan die heel logisch zijn. Bijvoorbeeld: bij Person een naam en een leeftijd, bij Room een kamernummer, etc. Uiteraard heb ik bij deze klassen dan ook getters en setters erbij geschreven. Ook wat zoek en verwijder functies voor klassen die een ArrayList bezitten. De reden waarom we niet meteen de klassen hebben geschreven volgens ons idee, is omdat ik nog niet veel wist over de nieuwe stof en dus een soort basis klassen systeem had gemaakt. De rest was bezig met het maken van een begin van de agenda. Aangezien we net 1 week 2DGraphics hadden gedaan moesten veel mensen heirna kijken om al stof te begrijpen die we nogniet hadden gehad. Later nadat het begin van de agenda was afgerond en er iets getekent kon worden, heb ik de code goed doorgekeken om het te begrijpen. Had zag er nog wat rommelig uit dus dit moest later nog opgeruimt worden.

## **Lesweek 3**
### *Reflectie proces*
Deze lesweek hebben we les gehad in het werken met ObjectIO. Het plan was dan om deze week ons data systeem op te zetten plus de bijbehorende DataWriter en DataReader. Ook moest de agenda verbeterd worden en moest er gezocht worden naar spritesheet plus het bouwen van een map. Deze taken hebben we allemaal kunnen verdelen. Ons idee was tijdens het werk elkaar te informeren over bepaalde keuzes dei gemaakt moesten worden. Aangezien we nog niet wisten hoe alles zou werken vonden we dit een goede manier van werken. Zo konden we meteen aan de slag en hulp vragen wanneer dat nodig was. De werksfeer was goed alleen kwam de discussie van het gebruik van het framework weer naar boven. Één lid was nog niet helemaal eens over het gebruiken van dit framework. Hij zag namelijk niet het voordeel er van in en vond het een beter idee om vanaf niets te beginnen en dit framework dus links laten liggen. We hebben verder hem niet kunnen "overhalen" en in principe nog geen keuze gemaakt. 

### *Reflectie vakinhoudelijk*
Deze lesweek hiervoor hebben goede uitleg gekregen over ObjectIO. Hierdoor hebben wij dus onze data systeem kunnen toepassen. Ik ging aan de slag met het opzetten van de data klassen. Zo is er een "hoofd" klasse waar al onze data uiteindelijk inkomt. Dit maakt het makkelijk om zo data op te slaan. Want dan hoef je maar naar één klasse te kijken, daar alles uithalen en dit allemaal opschrijven op één save file doormiddel van ObjectIO. Sjoerd had het idee om een "enum singleton" te maken voor de SavedData klasse. Ik had hier persoonlijk nog nooit van gehoord, dit zit ook niet tussen de lesstof die we hebben gehad. Ik had het opgezocht en het zag er makkelijk uit en het kwam met veel voordelen voor wat wij wouden doen.


    public enum SavedData {

        INSTANCE;

        private ArrayList<StudentData> studentData = new ArrayList<StudentData>();
        private ArrayList<TeacherData> teacherData = new ArrayList<TeacherData>();
        private ArrayList<LessonData> lessonData = new ArrayList<LessonData>();
        private ArrayList<GroupData> groupData = new ArrayList<GroupData>();

        // Getters and Setters
        public ArrayList<StudentData> getStudentData() {
            return studentData;
        }
        public void setStudentData(ArrayList<StudentData> studentData) {
            this.studentData = studentData;
        }

        public ArrayList<TeacherData> getTeacherData() {
            return teacherData;
        }
        public void setTeacherData(ArrayList<TeacherData> teacherData) {
            this.teacherData = teacherData;
        }

        public ArrayList<LessonData> getLessonData() {
            return lessonData;
        }
        public void setLessonData(ArrayList<LessonData> lessonData) {
            this.lessonData = lessonData;
        }

        public ArrayList<GroupData> getGroupData() {
        return groupData;
        }
        public void setGroupData(ArrayList<GroupData> groupData) {
            this.groupData = groupData;
        }
    }

Dit is hoe de code van de SavedData klasse eruit zit. De klasse is dus gevuld met ArrayLists die de aparte data van de student, teacher, lesson en group bijhouden. Deze zijn dan weer gevult met variabelen zoals: name, age, Gender, etc. 

Door zo een enum te maken met één "optie" erin kan je deze makkelijk overal aanroepen en krijg je toegang tot deze ArrayLists. Het grootste voordeel hiervan is dat hier maar één instantie van kan zijn. Zo kan er nooit een tweede SavedData enum gemaakt worden. En creeëren wij dus één plek waar alle data samen komt. Om deze data te bereiken kan je dus overal SavedData.INSTANCE schrijven en krijg je toegang tot all deze getters en setters van de data.

## **Lesweek 5**
### *Reflectie proces*
Deze week is er niet veel gedaan. Dit komt door het feit dat het framework dilemma weer naar boven is gekomen. In een vergadering met de tutor, heeft Timo duidelijk gemaakt dat hij nog steeds niet eens is over het gebruik van het framework van Sjoerd. We hebben dan ook een gesprek ingepland met Maurice om dit dilemma op te lossen. Zo hebben we 2 uren gepraat over wat wij nou eigenlijk wilde bereiken met deze proftaak. Tijdens dit gesprek kwam Maurice erachter dat het eigenlijk vooral ging om tussen een "strijd" tussen Sjoerd en Timo. Timo had het idee dat wat er in het framework gebeurde niet veel voordeel had tot geen voordeel had voor de proftaak en wilde alles vanaf niks zelf opbouwen. Maurice zei dat als je dat doet dat je dan uiteindelijk komt op het framework van Sjoerd. Wij vermelden ook dat het nu te laat zou zijn voor het niet gebruiken van het framework aangezien we al in week 5 zitten van de periode. Maurice heeft Sjoerd dan oko de opdracht te geven om samen met Timo aan iets te werken in de proftaak dat betrekking heeft tot het framework. Zo kan Timo vragen stellen over eventuele verwarringen en kunnen we toch gebruik maken en verder gaan met het voorgestelde framework van Sjoerd.

### *Reflectie vakinhoudelijk*
Zoals ik zei, is er niet veel gewerkt aan de proftaak aangezien het dilemma met het framework. Dus heb ik voornamelijk een klein beetje code op zitten ruimen en want comments toegevoegd aan bestaande code om het te verduidelijken. Volgende week zullen we het weer oppakken en verder gaan met waar we gebleven waren.

## **Lesweek 6**
### *Reflectie proces*
Deze week gingen we vooral nadenken over hoe het AI systeem gaat werken in onze simulatie. Sjoerd had ins snel ingeligt over zijn idee over hoe het AI zou moeten werken. Dit vonden we allemaal wel een goed idee en gingen er mee akkoord. Ook was de camera nog niet helemaal in orde van de simulatie. Voor de rest was er niet veel anders te doen. Wij kregen vaker dit idee bij deze proftaak. Vaak waren er paar opdrachten die uitgevoerd moesten worden alleen kon je deze niet opverdelen aan de projectleden. Dus moest er iemand aan de slag met iets en hadden de andere niet veel te doen.

### *Reflectie vakinhoudelijk*
De camera was nog niet helemaal in orde. Ik ging dus kijken of dat ik deze kon verbeteren. Heb hier even de tijd voor genomen en heb na veel inspiratie van de opdrachten van de 2DGraphics lessen, iets gemaakt. De nieuwe camera werkte perfect alleen zag dat als je de camera versleept, het beeld heel even soms vast liep. Blijkbaar moest werden alle plaatjes van de map apart getekent. Dit koste dus veel process power. Iemand is hier later nog naar gaan kijken en heeft dit kunnen oplossen. De camera lijkt in principe heel veel op die van de Angry Birds opdracht van 2DGraphics. Ik heb hem alleen aangepast zo dat hij goed werkt samen met de al bestaande code. 

## **Lesweek 7**
### *Reflectie proces*
We naderen al het einde van de periode en dus het einde van de proftaak. Sprites voor de NPC's waren al gevonden, ze moesten alleen nog getekent worden en kunnen bewegen. Ook moest de pathfinding van de NPC's gemaakt worden. Voor de rest moest er nog wat opgeruimt worden en wat comments toegevoegd worden. Vooral zat er veel werk in het goed maken van de pathfinding. Alweer hadden we het idee dat het werk niet goed verdeeld kon worden aangezien het maken van de pathfinding een nogal groot onderwerp is. Voor de rest ging de samenwerking goed net zoals altijd.

### *Reflectie vakinhoudelijk*
Ik ging aan de slag met maken van de NPC's dit deed ik samen met Teun. Hij ging meer het gedeelte doen van het tekenen van de NPC's en ik ging werken aan het bewegen van de NPC's. Eerst heb ik gekeken naar de movement die Johan van de opstart collega had vrij gemaakt. Hier werd echter gebruik gemaakt van een variabel "angle". Dit gaf de bewegende NPC's de mogelijkheid om een vrije rotatie te hebben. Voor onze simulatie willen wij dat de rotatie vast blijft. Daarom hebben ervoor gezorgt dat de gebruik maakt van andere sprites om zo aan te geven welke kant deze opkijkt. Ik moest dus een andere manier vinden om de movement te laten werken.   

    protected boolean moveTo(double deltaTime, Point2D target) {
        int moveDirectionX, moveDirectionY;
        if((int)target.getX() - (int)position.getX() < 0) {
            moveDirectionX = -1;
            direction = Direction.LEFT;
        } else if((int)target.getX() - (int)position.getX() > 0) {
            moveDirectionX = 1;
            direction = Direction.RIGHT;
        } else {
            moveDirectionX = 0;
        }

        if((int)target.getY() - (int)position.getY() < 0) {
            moveDirectionY = -1;
            direction = Direction.UP;
        } else if ((int)target.getY() - (int)position.getY() > 0) {
            moveDirectionY = 1;
            direction = Direction.DOWN;
        } else {
            moveDirectionY = 0;
        }

        if(moveDirectionX != 0 && moveDirectionY != 0) this.speed = diagonalSpeed;
        else this.speed = straightspeed;

        position.setLocation(position.getX() + moveDirectionX * deltaTime * speed, position.getY() + moveDirectionY * deltaTime * speed);

        if(target.getX() - position.getX() < 10 && target.getX() - position.getX() > -10 &&
            target.getY() - position.getY() < 10 && target.getY() - position.getY() > -10){
            return true;
        }
        return false;
    }

Dit is uiteindelijk de code waar ik op uit kwam. In principe is het een heel makkelijk stukje code. Ik bepaal wat de kant is waarop de NPC wilt lopen, door de target positie min de huidige positie te doen. Ik wil echter wil dat dit alleen de richting aan geeft dus wil ik het limiteren tot 1 of -1. Als ik dat niet zou doen dan gaat de NPC dus sneller hoe verder hij van de afstand is. Hierna check ik nog of dat de NPC schuin loopt. Als dit het geval is wil ik de snelheid slomer zetten (halveren). Anders zou de NPC 2x zo snel lopen wanneer hij schuin gaat. Daarna is het een kwestie van de locatie veranderen op basis van de deltaTime, zodat er geen verschil in zit wanneer je de simulatie sneller of slomer draait. Als allerlaatst wil ik nog checken of dat de NPC zijn target heeft bereikt zo ja dan return ik met een true om aan te geven dat hij zijn target heeft bereikt en anders return ik met een false, om het tegenovergestelde aan te geven.

## **Lesweek 8(+9)**
### *Reflectie proces*
Het einde is al in zicht en er moeten nog een aantal dingen gedaan worden. Ook is het extra nadelig aangezien we niet meer naar school kunnen om te werken aan het project. Alles zal dus nu vanaf thuis afgesproken moeten worden en uitgevoerd worden. Lars had een lijst afgesteld met dingen die we nog afgerond moeten worden. Zo was het duidelijk wat er dus nog allemaal afgerond of gemaakt moest worden. in week 4 moesten we stoppen met het werken aan de agenda. Echter hebben we wel oranje licht gekregen bij de demo van de agenda. Er moesten dus nog een aantal dingen aangepast worden en gemaakt worden. Hier mochten we dus alleen verder aan werken wanneer je al ver bent met de simulatie. Dit is uiteraard om te voorkomen dat je dadelijk geen tijd meer hebt voor de simulatie want dat is nou net waar het om gaat. Hiernaast waren er nog een aantal andere opdrachten die gedaan moesten worden die hebben de andere projectleden uitgevoerd. 

### *Reflectie vakinhoudelijk*
Mijn taak was dus om de agenda te verbeteren en om dingen eraan toe te voegen. Voornamelijk hadik het idee om een People Manager toe te voegen. Met het idee dat je studenten en docenten makkelijk kan verwijderen en toevoegen. Op papier had ik een schets gemaakt, die het idee gaf, hoe het eruit moet zien. 

![People Manager](images/peoplemanager.png)

Dit is uiteindelijk waar ik op uit kwam. Je kan makkelijk bij elke groep een student of docent selecteren en deze verwijderen door op de bijbehorende Delete knop te drukken. Een student of docent toevoegen gaat ook heel makkelijk door op de bovenstaande knoppen te drukken. Wanneer je op ADD STUDENT of ADD TEACHER drukt zal er nog een popup tevoorschijn komen waar je de gegevens invult. Wanneer je op Delete zou drukken en je hebt in de ComboBox een student of teacher geselecteerd, zal deze verwijderd worden uit de SavedData en wordt de ComboBox geupdate. Ook heb ik functies geschreven die duplicate code zo veel mogelijk weg halen. Zo is er een functie die een ComboBox maakt met daarnaast een delete knop. Die delete knop is dan ook meteen verbonden aan de ComboBox. Zo hoef ik niet 6 keer hetzelfde uit te schrijven.

    private FlowPane buildGroupRow(GroupData groupData){
        FlowPane flowPane = new FlowPane();
        ComboBox<String> group = new ComboBox<>();
        groupBoxes.add(group);
        updateGroupBox(group, groupData);
        group.setMaxWidth(125);
        group.setPrefWidth(125);
        flowPane.getChildren().add(group);
        Button deleteButton = new Button("Delete");
        deleteButton.setOnAction(event -> {removeStudentFromData(group.getValue()); updateGroupBox(group, groupData);});
        flowPane.getChildren().add(deleteButton);
        return flowPane;
    }

Dit is de code die dat mogelijk maakt. Zo wordt er een FlowPane gereturned met daarin de aangemaakt de ComboBox en de gelinkte delete knop. Om de ComboBoxes niet zich te laten aanpassen aan de grootte van de Strings die zich bevinden in de ComboBox. Zet ik de prefWidth en de maxWidth gelijk aan 125. Deze funcie kon echter niet gebruikt worden voor de Teachers ComboBox aangezien een Teacher niet in een Group zit. 

![Add Student](images/addstudent.png)

Dit is de popup van de ADD STUDENT knop. De ADD TEACHER knop laat in principe hetzelfde zien, alleen in plaats van StudentID, TeacherID en er is geen Group die je kan kiezen. Wanneer je op SAVE drukt in deze popup zal deze popup sluiten en zal de ComboBox die bij de geselecteerde group hoort, updaten en de nieuwe student of teacher hebben toegevoegd. Deze GUI keuzes zijn naar mijn mening heel overzichtelijk en geven makkelijk aan wat er verwacht wordt van de gebruiker. Ook vind ik het er goed uitzien en is het niet een stomme tabel waar alles er recht toe recht aan in staat.

## **Reflectie op stelling**
*In het bedrijfsleven wordt gebruik gemaakt van JavaFX.*

JavaFX is een software platform for het ontwikkelen van desktop applicaties, die op allerlei systemen kunnen draaien. JavaFX eerste release was op december 4 2008. JavaFX is gemaakt om de toen al bestaande Swing te vervangen, als de standaard GUI library voor Standard Edition van Java. Het is sinds die tijd, nog steeds de standaard voor de GUI library. De huidige laatste stable release is op maart 14 2020. In het begin, begon JavaFX als een aparte scripting language maar dit is daarna veranderd en kan je JavaFX gewoon gebruiken met Java.

JavaFX is misschien wel een van de beste libraries voor het bouwen van gebruikersvriendelijke applicaties die op Windows maar ook op Mac OS X en Linux kunnen draaien. Waarom JavaFX over ADF of APEX? JavaFX is de standaard Java API waarmee makkelijk verschillende user interfaces gemaakt kunnen worden. Ook heeft JavaFX niet veel nodig om te draaien, hierdoor kan JavaFX dus op veel verschillende plekken draaien waaronder zelfs een raspberry PI. 

JavaFX kan gebruikt worden voor allerlei diverse opdrachten. Zo kan JavaFX gebruikt worden voor doelen zoals: grafieken, tabellen, 3D-figuren en animaties, voortgangsbalkjes, etc. Dit maakt JavaFX een heel efficiënt en robuuste manier van het maken van grafische onderdelen. Er zijn ook een hoop hulp middelen gebouwd, die het maken van user interfaces nog makkelijker maken. Deze voordelen maken werken met JavaFX heel aantrekkelijk. Daarom wordt JavaFX nog steeds gebruikt in allerlei diverse projecten in het bedrijfsleven. 

Dus JavaFX is in de al sinds 2008 de standaard geworden in de Java Standard Edition, voor de library voor de GUI. JavaFX is een heel efficiënt en robuuste manier van werken door de diverse mogelijkheden die je hebt voor het maken van grafische elemeten. JavaFX heeft niet veel nodig om te draaien en kan dus ook draaien op bijvoorbeeld een Raspberry PI. Als laatst is JavaFX te gebruiken met Java waardoor het een zeer makkelijke manier van werken is. Door all deze voordelen is JavaFX nog steeds de standaard en wordt het nog veel gebruikt door veel bedrijven. 

*Bronvermelding*
- JavaFX is growing... (2015, 11 augustus). Geraadpleegd op 5 april 2020, van https://www.transfer-solutions.com/javafx-is-growing/
- Wikipedia contributors. (2020, 27 maart). JavaFX. Geraadpleegd op 5 april 2020, van https://en.wikipedia.org/wiki/JavaFX

## **Lijst met applicaties die gebruik maken van JSON**
-   Twitter
-   Facebook
-   Google Maps
-   Github
-   MySQL

JSON is een notatie voor objecten in de syntax van JavaScript. Het is een afgesproken standaard om bepaalde objecten op te slaan en uit te lezen. JSON wordt vooral veel gebruikt bij diverse websites die dynamische elementen gebruiken. JSON is dan wel in de syntax geschreven van JavaScript echter betekent dit niet dat JSON taal afhankelijk is. Helaas heeft JSON geen andere schema gerelateerde functies zoals die wel te vinden zijn in bijvoorbeeld XML. Wat JSON zo populair maakt is dat het een overzichtelijke tekst based manier van noteren heeft. Zo is het makkelijk te ontleden en verreist het geen extra code. JSON is dus een snelle manier van het uitwisselen van gegevens. Dit is dus de reden waarom het gebruikt wordt bij zulke grote websites en applicaties die heel snel moeten kunnen draaien.


