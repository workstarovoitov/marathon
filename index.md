<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=0.5">
    <script src='src/phaser-arcade-physics.min.js'></script>
</head>
<body>

    <script>

    var Preloader = new Phaser.Class({

        Extends: Phaser.Scene,

        initialize:

        function Preloader ()
        {
            Phaser.Scene.call(this, 'preloader');
        },

        preload: function ()
        {
 
            this.load.image('imgHeadbandMain0', 'assets/sprites/headbandMain0.png');
            this.load.image('imgHeadbandMain2', 'assets/sprites/headbandMain2.png');
            this.load.image('imgHeadbandScene7', 'assets/sprites/headbandScene7.png');
            this.load.image('imgDeskOpened', 'assets/sprites/shelf.png');
            this.load.image('imgBook', 'assets/sprites/book.png');
            this.load.image('imgClock', 'assets/sprites/clock.png');
            this.load.image('imgTracker', 'assets/sprites/tracker.png');

            this.load.image('imgM1', 'assets/sprites/calendar/m1.png');
            this.load.image('imgM2', 'assets/sprites/calendar/m2.png');
            this.load.image('imgM3', 'assets/sprites/calendar/m3.png');
            this.load.image('imgM4', 'assets/sprites/calendar/m4.png');
            this.load.image('imgM5', 'assets/sprites/calendar/m5.png');
            this.load.image('imgM6', 'assets/sprites/calendar/m6.png');
            this.load.image('imgM7', 'assets/sprites/calendar/m7.png');
            this.load.image('imgM8', 'assets/sprites/calendar/m8.png');
            this.load.image('imgM9', 'assets/sprites/calendar/m9.png');
            this.load.image('imgM10', 'assets/sprites/calendar/m10.png');
            this.load.image('imgM11', 'assets/sprites/calendar/m11.png');
            this.load.image('imgM12', 'assets/sprites/calendar/m12.png');
            this.load.image('imgD0', 'assets/sprites/calendar/0.png');
            this.load.image('imgD1', 'assets/sprites/calendar/1.png');
            this.load.image('imgD2', 'assets/sprites/calendar/2.png');
            this.load.image('imgD3', 'assets/sprites/calendar/3.png');
            this.load.image('imgD4', 'assets/sprites/calendar/4.png');
            this.load.image('imgD5', 'assets/sprites/calendar/5.png');
            this.load.image('imgD6', 'assets/sprites/calendar/6.png');
            this.load.image('imgD7', 'assets/sprites/calendar/7.png');
            this.load.image('imgD8', 'assets/sprites/calendar/8.png');
            this.load.image('imgD9', 'assets/sprites/calendar/9.png');

            this.load.image('imgBoardScene5', 'assets/sprites/boardScene5.png');
            this.load.image('imgWardrobeScene5', 'assets/sprites/wardrobeScene5.png');
            this.load.image('imgWardrobeSceneMain2', 'assets/sprites/wardrobeSceneMain2.png');
            this.load.image('imgShirtScene5', 'assets/sprites/shirtScene5.png');
            this.load.image('imgShoesRScene5', 'assets/sprites/shoesRScene5.png');
            this.load.image('imgShoesWScene5', 'assets/sprites/shoesWScene5.png');
            this.load.image('imgPoloGScene5', 'assets/sprites/poloGScene5.png');
            this.load.image('imgPoloRScene5', 'assets/sprites/poloRScene5.png');
            this.load.image('imgPoloBScene5', 'assets/sprites/poloBScene5.png');
            this.load.image('imgHatScene5', 'assets/sprites/hatScene5.png');
            
            this.load.image('imgReady', 'assets/sprites/ready.png');
            this.load.image('imgSteady', 'assets/sprites/steady.png');
            this.load.image('imgGo', 'assets/sprites/go.png');
            this.load.image('imgFaster', 'assets/sprites/faster.png');
            this.load.image('imgGood', 'assets/sprites/good.png');
            this.load.image('imgStep', 'assets/sprites/run3.png');

            this.load.image('imgFlag', 'assets/sprites/flagScene8.png');
            this.load.image('imgFlag2', 'assets/sprites/flagMainScene2.png');
            this.load.image('imgTrack1', 'assets/sprites/track1.png');
           

            this.load.image('imgPantsSceneMain2', 'assets/sprites/pantsSceneMain2.png');
            this.load.image('imgPantsScene9', 'assets/sprites/pantsScene9.png');
   
            this.load.audio('mp3stepL', 'assets/sound/stepL.mp3');
            this.load.audio('mp3stepR', 'assets/sound/stepR.mp3');
            this.load.audio('mp3breath', 'assets/sound/breath.mp3');
            this.load.audio('mp3fanfair', 'assets/sound/fanfair.mp3');

            this.load.audio('mp3bag', 'assets/sound/bag.mp3');
            this.load.audio('mp3drawerClose', 'assets/sound/drawerClose.mp3');
            this.load.audio('mp3drawerOpen', 'assets/sound/drawerOpen.mp3');
            this.load.audio('mp3Bttn', 'assets/sound/bttn.mp3');
            this.load.audio('mp3cock', 'assets/sound/cock.mp3');

            this.load.audio('mp3SoundBttn', 'assets/sound/soundBttn.mp3');
            this.load.audio('mp3yawn', 'assets/sound/yawn.mp3');
            this.load.audio('mp3zip', 'assets/sound/zip.mp3');
            this.load.audio('mp3unzip', 'assets/sound/unzip.mp3');
            this.load.audio('mp3wOpen', 'assets/sound/wardrobeOpen.mp3');
            this.load.audio('mp3wClose', 'assets/sound/wardrobeClose.mp3');
           
            this.load.audio('mp3ambient', 'assets/ambient/Ketsa.mp3');
            this.load.audio('mp3run', 'assets/ambient/run.mp3');
            this.load.audio('mp3treadmill', 'assets/ambient/treadmill.mp3');
            
            this.load.image('book1.0', 'assets/books/1.0.jpg');
            this.load.image('book1.1', 'assets/books/1.1.jpg');
            this.load.image('book1.2', 'assets/books/1.2.jpg');
            this.load.image('book2.0', 'assets/books/2.0.jpg');
            this.load.image('book2.1', 'assets/books/2.1.jpg');
            this.load.image('book2.2', 'assets/books/2.2.jpg');
            this.load.image('book3.0', 'assets/books/3.0.jpg');
            this.load.image('book3.1', 'assets/books/3.1.jpg');
            this.load.image('book3.2', 'assets/books/3.2.jpg');

            this.load.image('imgStartBG', 'assets/background/start.jpg');
            this.load.image('imgWakeUp', 'assets/background/sceneMain0.jpg');
            this.load.image('imgMainSceneLeft', 'assets/background/sceneMain1.jpg');
            this.load.image('imgMainSceneRight', 'assets/background/sceneMain2.jpg');
            this.load.image('imgBoard', 'assets/background/scene1.jpg');
            this.load.image('imgDeskClosed', 'assets/background/scene2.1.jpg');
            this.load.image('imgLaptop', 'assets/background/scene3.jpg');
            this.load.image('imgShelf', 'assets/background/scene4.jpg');
            this.load.image('imgWardrobe', 'assets/background/scene5.jpg');
            this.load.image('imgSportsbag', 'assets/background/scene6.jpg');
            this.load.image('imgTreadmill', 'assets/background/scene7.jpg');
            this.load.image('imgMap', 'assets/background/scene8.jpg');
            this.load.image('imgBed', 'assets/background/scene9.jpg');

        },

        create: function ()
        {
            this.scene.start('StartScene');
            ambient = this.sound.add('mp3ambient',  { loop: 1, volume: 0.05 });      
            click = this.sound.add('mp3SoundBttn', { volume: 2 });
        }
        

    });

        var StartScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

            function StartScene ()
            {
                Phaser.Scene.call(this, { key: 'StartScene', active: true });
            },
            create: createStartScene

        });

        var MainScene0 = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

            function MainScene0 ()
            {
                Phaser.Scene.call(this, { key: 'MainScene0', active: false });
            },
            preload: preloadMainScene0,
            create: createMainScene0,
            update: updateMainScene0

        });

        var MainSceneL = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

            function MainSceneL ()
            {
                Phaser.Scene.call(this, { key: 'MainSceneL', active: false });
            },
            preload: preloadMainSceneL,
            create: createMainSceneL,
            update: updateMainSceneL

        });

        var MainSceneR = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

            function MainSceneL ()
            {
                Phaser.Scene.call(this, { key: 'MainSceneR', active: false });
            },
            preload: preloadMainSceneR,
            create: createMainSceneR,
            update: updateMainSceneR

        });

        var WardrobeScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function WardrobeScene ()
            {
                    Phaser.Scene.call(this, { key: 'WardrobeScene', active: false });
            },
            preload: preloadWardrobeScene,
            create: createWardrobeScene,
            update: updateWardrobeScene

        });

        var SportsbagScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function SportsbagScene ()
            {
                    Phaser.Scene.call(this, { key: 'SportsbagScene', active: false });
            },
            preload: preloadSportsbagScene,
            create: createSportsbagScene,
            update: updateSportsbagScene

        });

        var TreadmillScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function TreadmillScene ()
            {
                    Phaser.Scene.call(this, { key: 'TreadmillScene', active: false });
            },
            preload: preloadTreadmillScene,
            create: createTreadmillScene,
            update: updateTreadmillScene

        });

        var BedScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function BedScene ()
            {
                    Phaser.Scene.call(this, { key: 'BedScene', active: false });
            },
            preload: preloadBedScene,
            create: createBedScene,
            update: updateBedScene

        });

        var MapScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function MapScene ()
            {
                    Phaser.Scene.call(this, { key: 'MapScene', active: false });
            },
            //preload: preloadBedScene,
            create: createMapScene,
            update: updateMapScene

        });

        var BoardScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function BoardScene ()
            {
                    Phaser.Scene.call(this, { key: 'BoardScene', active: false });
            },
            //preload: preloadBedScene,
            create: createBoardScene,
            update: updateBoardScene

        });

        var ShelfScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function ShelfScene ()
            {
                    Phaser.Scene.call(this, { key: 'ShelfScene', active: false });
            },
            //preload: preloadBedScene,
            create: createShelfScene,
            update: updateShelfScene

        });

        var LaptopScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function LaptopScene ()
            {
                    Phaser.Scene.call(this, { key: 'LaptopScene', active: false });
            },
            //preload: preloadBedScene,
            create: createLaptopScene,
            update: updateLaptopScene

        });

        var DeskScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function DeskScene ()
            {
                    Phaser.Scene.call(this, { key: 'DeskScene', active: false });
            },
            //preload: preloadBedScene,
            create: createDeskScene,
            update: updateDeskScene

        });

        var config = {
            type: Phaser.AUTO,
            backgroundColor: 'white',
            scale: {
                mode: Phaser.Scale.FIT,
            parent: 'phaser-example',
            width: 1920,
            height: 1080,
            min: {
                width: 800,
                height: 600
            },
            max: {
                width: 1920,
                height: 1080
            }
            },
            scene: [Preloader, LaptopScene, DeskScene, ShelfScene, BoardScene, MapScene, BedScene, TreadmillScene, SportsbagScene, WardrobeScene, MainSceneR, MainSceneL, MainScene0, StartScene],
            audio: { disableWebAudio: true }
        };

        var g_month = 0;
        var g_dayH = 2;
        var g_dayL = 9;
        var FlagsScene8XY_win = [[475, 330], [294, 425], [288, 377], [258, 482]];
        var FlagsScene8XY = [[475, 400], [294, 425], [288, 377], [258, 482]];

        var ambient;    
        var cick;    
        var ambientOn = false;    
        var shelfWin = true;    
        var sportsbagOpen = true;    
        var wardrobeOpen = false;    
        var shelfOpen = false;    
        var treadmillRun = false;
        var timerTreadmill;

        var headbandPacked = false;
        var hatPacked = false;
        var shoesRPacked = false;
        var shoesWPacked = false;
        var poloGPacked = false;
        var poloRPacked = false;
        var poloBPacked = false;
        var shirtPacked = false;
        var clockPacked = false;
        var armbandPacked = false;
        var trackerPacked = false;
        var pantsPacked = false;

        var game = new Phaser.Game(config);

        function createStartScene() {

            imgStartScene = this.add.image(0, 0, 'imgStartBG').setOrigin(0);
          
            this.input.on('pointerdown', function (pointer, gameObject) {
                //this.scene.switch('MainScene0');

                this.cameras.main.fadeOut(1000);
                timedEvent = this.time.addEvent({ delay: 1250, callback: () => { this.scene.start('MainScene0'); }, callbackScope: this, repeat: 0, startAt: 0 });

            }, this);

        }


        function preloadMainScene0()
        {

        }

        function preloadMainSceneL() {
            //this.load.audio('mp3cock', 'assets/sound/cock.wav');
        }

        function preloadMainSceneR() {
            //this.load.audio('mp3cock', 'assets/sound/cock.wav');
        }

        function preloadWardrobeScene() {

        }

        function preloadSportsbagScene() {

        }

        

        function preloadTreadmillScene() {

        }

        function preloadBedScene() {

        }




        function createMainScene0()
        {

            this.add.image(0, 0, 'imgWakeUp').setOrigin(0).setScale(1);

            this.cameras.main.fadeIn(6000);

            var fxCock = this.sound.add('mp3cock');
            fxCock.play(); 
        
            var sprite_mainLeft = this.add.sprite(0, 0); 
            var sprite_mainRight = this.add.sprite(0, 0); 
            var sprite_wardrobe = this.add.sprite(0, 0); 
            var sprite_soundBox = this.add.sprite(0, 0);
            var sprite_headBand = this.add.sprite(1255, 603, 'imgHeadbandMain0').setOrigin().setScale(1);
     
            if (headbandPacked) {
                sprite_headBand.visible = false;
                sprite_headBand.disableInteractive();
            } else {
                sprite_headBand.visible = true;
                sprite_headBand.setInteractive();
            }

            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0,          500, 0,     500, 850,       0, 850]);
            var plgn_mainRight = new Phaser.Geom.Polygon([1100, 0,      1920, 0,    1920, 850,      1100, 850]);
            var plgn_wardrobe = new Phaser.Geom.Polygon([550, 0,        1050, 0,    1050, 900,       550, 900]);
            var plgn_soundBox = new Phaser.Geom.Polygon([1550, 700,     1920, 700,  1920, 900,      1550, 900]);
       
            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_mainLeft.points, true);
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_mainRight.points, true);
            //graphics.fillStyle(0xffaaaa);
            //graphics.fillPoints(plgn_wardrobe.points, true);
            //graphics.fillStyle(0xffaaff);
            //graphics.fillPoints(plgn_soundBox.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;
        
            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_mainRight.setInteractive(plgn_mainRight, Phaser.Geom.Polygon.Contains);
            sprite_wardrobe.setInteractive(plgn_wardrobe, Phaser.Geom.Polygon.Contains);
            sprite_soundBox.setInteractive(plgn_soundBox, Phaser.Geom.Polygon.Contains);


            sprite_headBand.on('pointerdown', function (pointer, gameObject) {

                sprite_headBand.disableInteractive();
                sprite_headBand.visible = false;
                headbandPacked = true;
                hatPacked = false;
                fxBag = this.sound.add('mp3bag');
                fxBag.play();         
            }, this);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('MainSceneL');

            },this);

            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {

                this.scene.start('MainSceneR');

           },this);

            sprite_wardrobe.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('WardrobeScene');

            },this);

            sprite_soundBox.on('pointerdown', function (pointer, gameObject) {
                playAmbient();
            }, this);

  
    }
 
        function createMainSceneL()
        {

            var imgScene = this.add.image(0, 0, 'imgMainSceneLeft').setOrigin(0);
          
            var sprite_mainRight = this.add.sprite(0, 0); 
            var sprite_wardrobe = this.add.sprite(0, 0); 
            var sprite_books = this.add.sprite(0, 0);
            var sprite_board = this.add.sprite(0, 0);
            var sprite_desk = this.add.sprite(0, 0);
            var sprite_laptop = this.add.sprite(0, 0);
            var sprite_shelf = this.add.sprite(0, 0);
       
            var plgn_mainRight = new Phaser.Geom.Polygon([1570, 0,      1920, 0,    1920, 1080,      1570, 1080]);
            var plgn_wardrobe = new Phaser.Geom.Polygon([1100, 0,        1550, 0,    1550, 680,       1100, 680]);
            var plgn_books = new Phaser.Geom.Polygon([950, 0,     1150, 0,  1150, 100,      950, 100]);
            var plgn_board = new Phaser.Geom.Polygon([270, 0,     1030, 140,  1020, 570,      280, 630]);
            var plgn_desk = new Phaser.Geom.Polygon([180, 700,     1080, 600,  1360, 700,      1360, 1080,  180, 1080]);
            var plgn_laptop = new Phaser.Geom.Polygon([710, 610,     860, 570,  1030, 710,      910, 760,   750, 730]);
            var plgn_shelf = new Phaser.Geom.Polygon([350, 890,     790, 820,  790, 1080,      350, 1080]);
       
            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_mainRight.points, true);
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_mainRight.points, true);
            //graphics.fillStyle(0xffaaaa);
            //graphics.fillPoints(plgn_wardrobe.points, true);
            //graphics.fillStyle(0xffaaff);
            //graphics.fillPoints(plgn_books.points, true);
            //graphics.fillStyle(0xffaaff);
            //graphics.fillPoints(plgn_board.points, true);
            //graphics.fillStyle(0xaafaff);
            //graphics.fillPoints(plgn_desk.points, true);
            //graphics.fillStyle(0x00aaff);
            //graphics.fillPoints(plgn_laptop.points, true);
            //graphics.fillStyle(0xff00ff);
            //graphics.fillPoints(plgn_shelf.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;
        
            sprite_mainRight.setInteractive(plgn_mainRight, Phaser.Geom.Polygon.Contains);
            sprite_wardrobe.setInteractive(plgn_wardrobe, Phaser.Geom.Polygon.Contains);
            sprite_books.setInteractive(plgn_books, Phaser.Geom.Polygon.Contains);
            sprite_board.setInteractive(plgn_board, Phaser.Geom.Polygon.Contains);
            sprite_desk.setInteractive(plgn_desk, Phaser.Geom.Polygon.Contains);
            sprite_laptop.setInteractive(plgn_laptop, Phaser.Geom.Polygon.Contains);
            sprite_shelf.setInteractive(plgn_shelf, Phaser.Geom.Polygon.Contains);


            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {

                this.scene.start('MainSceneR');

            }, this);

            sprite_wardrobe.on('pointerdown', function (pointer, gameObject) {
          
                this.scene.switch('WardrobeScene');

            },this);

            sprite_books.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('BooksSceneL');
            }, this);

            sprite_board.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('BoardScene');

            }, this);

            sprite_desk.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('DeskScene');

            }, this);

            sprite_laptop.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('LaptopScene');

            }, this);

            sprite_shelf.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('ShelfScene');

            }, this);


    }
 
        function createMainSceneR()
        {

            this.add.image(0, 0, 'imgMainSceneRight').setOrigin(0);
            this.add.image(385, 0, 'imgWardrobeSceneMain2').setOrigin(0).setScale(1);
            this.add.image(1500, 300, 'imgFlag2').setOrigin(0).setScale(0.33);

            var sprite_treadmill = this.add.sprite(0, 0); 
            var sprite_wardrobe = this.add.sprite(0, 0); 
            var sprite_mainLeft = this.add.sprite(0, 0); 
            var sprite_sportsBag = this.add.sprite(0, 0); 
            var sprite_soundBox = this.add.sprite(0, 0); 
            var sprite_books = this.add.sprite(0, 0); 
            var sprite_bed = this.add.sprite(0, 0); 
            var sprite_map = this.add.sprite(0, 0); 
            var sprite_headBand = this.add.sprite(1002, 578, 'imgHeadbandMain2').setOrigin().setScale(1);
            var sprite_pants = this.add.sprite(1580, 860, 'imgPantsSceneMain2').setOrigin(0).setInteractive();

            if (headbandPacked) {
                sprite_headBand.visible = false;
                sprite_headBand.disableInteractive();
            } else {
                sprite_headBand.visible = true;
                sprite_headBand.setInteractive();
            }

            if (pantsPacked) {
                sprite_pants.visible = false;
                sprite_pants.disableInteractive();
            } else {
                sprite_pants.visible = true;
                sprite_pants.setInteractive();
            }

            var plgn_treadmill = new Phaser.Geom.Polygon([700, 0, 1100, 0, 1100, 1080, 700, 1080]);
            var plgn_wardrobe = new Phaser.Geom.Polygon([0, 0, 500, 0, 500, 1080, 0, 1080]);
            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 530, 230, 530, 230, 930, 1400, 930, 1400, 1080, 0, 1080]);
            var plgn_sportsBag = new Phaser.Geom.Polygon([440, 770, 580, 700, 700, 700, 700, 840, 570, 920, 440, 910]);
            var plgn_soundBox = new Phaser.Geom.Polygon([1280, 590, 1420, 590, 1420, 700, 1280, 690]);
            var plgn_books = new Phaser.Geom.Polygon([1250, 720, 1400, 720, 1400, 820, 1250, 820]);
            var plgn_bed = new Phaser.Geom.Polygon([1400, 930, 1630, 530, 1920, 530, 1920, 1080, 1400, 1080]);
            var plgn_map = new Phaser.Geom.Polygon([1250, 100, 1750, 100, 1750, 500, 1250, 500]);

            
            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xff00aa);
            //graphics.fillPoints(plgn_treadmill.points, true);
            //graphics.fillStyle(0xffaaaa);
            //graphics.fillPoints(plgn_wardrobe.points, true);
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_mainLeft.points, true);
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_sportsBag.points, true);
            //graphics.fillStyle(0xffaaff);
            //graphics.fillPoints(plgn_soundBox.points, true);
            //graphics.fillStyle(0xaaaaff);
            //graphics.fillPoints(plgn_books.points, true);
            //graphics.fillStyle(0xaaaa00);
            //graphics.fillPoints(plgn_bed.points, true);
            //graphics.fillStyle(0xaaeaee);
            //graphics.fillPoints(plgn_map.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;
        
            sprite_treadmill.setInteractive(plgn_treadmill, Phaser.Geom.Polygon.Contains);
            sprite_wardrobe.setInteractive(plgn_wardrobe, Phaser.Geom.Polygon.Contains);
            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_sportsBag.setInteractive(plgn_sportsBag, Phaser.Geom.Polygon.Contains);
            sprite_soundBox.setInteractive(plgn_soundBox, Phaser.Geom.Polygon.Contains);
            sprite_books.setInteractive(plgn_books, Phaser.Geom.Polygon.Contains);
            sprite_bed.setInteractive(plgn_bed, Phaser.Geom.Polygon.Contains);
            sprite_map.setInteractive(plgn_map, Phaser.Geom.Polygon.Contains);

           // if (!headBandPacked) {
           //     var sprite_headBand = this.add.sprite(1460, 910, 'imgPinUnconnected').setOrigin().setScale(1).setInteractive();
           //     this.input.setDraggable(sprite_headBand);
           // }

            sprite_treadmill.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('TreadmillScene');
            },this);

            sprite_wardrobe.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('WardrobeScene');
            },this);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('MainSceneL');

            }, this);

            sprite_sportsBag.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('SportsbagScene');
            }, this);

            sprite_soundBox.on('pointerdown', function (pointer, gameObject) {
                playAmbient();
            }, this);

            sprite_books.on('pointerdown', function (pointer, gameObject) {
               
                
            }, this);

            sprite_bed.on('pointerdown', function (pointer, gameObject) {

                this.scene.start('BedScene');

            }, this);

            sprite_map.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('MapScene');

            }, this);

            sprite_headBand.on('pointerdown', function (pointer, gameObject) {

                sprite_headBand.disableInteractive();
                sprite_headBand.visible = false;
                headbandPacked = true;
                hatPacked = false;
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_pants.on('pointerdown', function (pointer, gameObject) {

                sprite_pants.disableInteractive();
                sprite_pants.visible = false;
                pantsPacked = true;
                fxBag = this.sound.add('mp3bag');
                fxBag.play();

            }, this);

    }

        function createWardrobeScene()
        {

            this.add.image(0, 0, 'imgWardrobe').setOrigin(0);
            this.add.image(150, 380, 'imgBoardScene5').setOrigin(0);

            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_mainRight = this.add.sprite(0, 0);
            var sprite_wardrobe = this.add.sprite(0, 0);
            var sprite_books = this.add.sprite(0, 0);

            var sprite_hat = this.add.sprite(1142, 343, 'imgHatScene5').setOrigin().setScale(1).setInteractive();
            var sprite_shoesR = this.add.sprite(1000, 900, 'imgShoesRScene5').setOrigin().setScale(1).setInteractive();
            var sprite_shoesW = this.add.sprite(1152, 910, 'imgShoesWScene5').setOrigin().setScale(1).setInteractive();
            var sprite_poloB = this.add.sprite(1200, 660, 'imgPoloBScene5').setOrigin().setScale(1).setInteractive();
            var sprite_poloR = this.add.sprite(1144, 658, 'imgPoloRScene5').setOrigin().setScale(1).setInteractive();
            var sprite_poloG = this.add.sprite(1103, 655, 'imgPoloGScene5').setOrigin().setScale(1).setInteractive();
            var sprite_shirt = this.add.sprite(1011, 641, 'imgShirtScene5').setOrigin().setScale(1).setInteractive();

            sprite_hat.visible = false;
            sprite_shoesR.visible = false;
            sprite_shoesW.visible = false;
            sprite_poloG.visible = false;
            sprite_poloB.visible = false;
            sprite_poloR.visible = false;
            sprite_shirt.visible = false;
            
            var sprite_wardrobeDoor = this.add.sprite(1070, 540, 'imgWardrobeScene5').setOrigin().setScale(1).setInteractive();

            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 500, 0, 500, 1080, 0, 1080]);
            var plgn_mainRight = new Phaser.Geom.Polygon([1350, 0, 1920, 0, 1920, 1080, 1350, 1080]);
            var plgn_wardrobe = new Phaser.Geom.Polygon([500, 0, 1350, 0, 1350, 1080, 500, 1080]);
            var plgn_books = new Phaser.Geom.Polygon([300, 100, 520, 100, 520, 320, 300, 320]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_mainLeft.points, true);
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_mainRight.points, true);
            //graphics.fillStyle(0xffaaaa);
            //graphics.fillPoints(plgn_wardrobe.points, true);
            //graphics.fillStyle(0xffaaff);
            //graphics.fillPoints(plgn_books.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_mainRight.setInteractive(plgn_mainRight, Phaser.Geom.Polygon.Contains);
            sprite_wardrobe.setInteractive(plgn_wardrobe, Phaser.Geom.Polygon.Contains);
            sprite_books.setInteractive(plgn_books, Phaser.Geom.Polygon.Contains);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                if (wardrobeOpen) {
                    fxWardrobe = this.sound.add('mp3wClose');
                    fxWardrobe.play();
                    wardrobeOpen = false;
                }
                this.scene.start('MainSceneL');

            }, this);
            
            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {
                if (wardrobeOpen) {
                    fxWardrobe = this.sound.add('mp3wClose');
                    fxWardrobe.play();
                    wardrobeOpen = false;
                }
                this.scene.start('MainSceneR');

            }, this);

            sprite_wardrobe.on('pointerdown', function (pointer, gameObject) {

                var fxWardrobe;
                if (wardrobeOpen) {
                    fxWardrobe = this.sound.add('mp3wClose');
                   
                    sprite_wardrobeDoor.visible = true;
                    sprite_wardrobeDoor.setInteractive();
                } else {
                    fxWardrobe = this.sound.add('mp3wOpen');
                    if (!hatPacked) {
                        sprite_hat.visible = true;
                        sprite_hat.setInteractive();
                    }
                    if (!shoesRPacked) {
                        sprite_shoesR.visible = true;
                        sprite_shoesR.setInteractive();
                    }
                    if (!shoesWPacked) {
                        sprite_shoesW.visible = true;
                        sprite_shoesW.setInteractive();
                    }
                    if (!poloGPacked) {
                        sprite_poloG.visible = true;
                        sprite_poloG.setInteractive();
                    }
                    if (!poloBPacked) {
                        sprite_poloB.visible = true;
                        sprite_poloB.setInteractive();
                    }
                    if (!poloRPacked) {
                        sprite_poloR.visible = true;
                        sprite_poloR.setInteractive();
                    }
                    if (!shirtPacked) {
                        sprite_shirt.visible = true;
                        sprite_shirt.setInteractive();
                    }                   
                    
                    sprite_wardrobeDoor.visible = false;
                    sprite_wardrobeDoor.disableInteractive();
                }

                fxWardrobe.play();
                wardrobeOpen = !wardrobeOpen;

            }, this);
  
            sprite_wardrobeDoor.on('pointerdown', function (pointer, gameObject) {

                var fxWardrobe;
                if (wardrobeOpen) {
                    fxWardrobe = this.sound.add('mp3wClose');
                   
                    sprite_wardrobeDoor.visible = true;
                    sprite_wardrobeDoor.setInteractive();
                } else {
                    fxWardrobe = this.sound.add('mp3wOpen');
                    if (!hatPacked) {
                        sprite_hat.visible = true;
                        sprite_hat.setInteractive();
                    }
                    if (!shoesRPacked) {
                        sprite_shoesR.visible = true;
                        sprite_shoesR.setInteractive();
                    }
                    if (!shoesWPacked) {
                        sprite_shoesW.visible = true;
                        sprite_shoesW.setInteractive();
                    }
                    if (!poloGPacked) {
                        sprite_poloG.visible = true;
                        sprite_poloG.setInteractive();
                    }
                    if (!poloBPacked) {
                        sprite_poloB.visible = true;
                        sprite_poloB.setInteractive();
                    }
                    if (!poloRPacked) {
                        sprite_poloR.visible = true;
                        sprite_poloR.setInteractive();
                    }
                    if (!shirtPacked) {
                        sprite_shirt.visible = true;
                        sprite_shirt.setInteractive();
                    }                   
                    
                    sprite_wardrobeDoor.visible = false;
                    sprite_wardrobeDoor.disableInteractive();
                }

                fxWardrobe.play();
                wardrobeOpen = !wardrobeOpen;

            }, this);
  

            sprite_hat.on('pointerdown', function (pointer, gameObject) {

                hatPacked = true;
                headbandPacked = false;
                sprite_hat.visible = false;
                sprite_hat.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();         

            }, this);

            sprite_shoesR.on('pointerdown', function (pointer, gameObject) {

                shoesRPacked = true;
                sprite_shoesR.visible = false;
                sprite_shoesR.disableInteractive();

                shoesWPacked = false;
                sprite_shoesW.visible = true;
                sprite_shoesW.setInteractive();

                fxBag = this.sound.add('mp3bag');
                fxBag.play();         

            }, this);

            sprite_shoesW.on('pointerdown', function (pointer, gameObject) {

                shoesWPacked = true;
                sprite_shoesW.visible = false;
                sprite_shoesW.disableInteractive();

                shoesRPacked = false;
                sprite_shoesR.visible = true;
                sprite_shoesR.setInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();         

            }, this);

            sprite_poloG.on('pointerdown', function (pointer, gameObject) {

                poloGPacked = true;
                sprite_poloG.visible = false;
                sprite_poloG.disableInteractive();

                poloRPacked = false;
                sprite_poloR.visible = true;
                sprite_poloR.setInteractive();

                poloBPacked = false;
                sprite_poloB.visible = true;
                sprite_poloB.setInteractive();

                shirtPacked = false;
                sprite_shirt.visible = true;
                sprite_shirt.setInteractive();

                fxBag = this.sound.add('mp3bag');
                fxBag.play();         

            }, this);

            sprite_poloR.on('pointerdown', function (pointer, gameObject) {

                poloRPacked = true;
                sprite_poloR.visible = false;
                sprite_poloR.disableInteractive();

                poloGPacked = false;
                sprite_poloG.visible = true;
                sprite_poloG.setInteractive();

                poloBPacked = false;
                sprite_poloB.visible = true;
                sprite_poloB.setInteractive();

                shirtPacked = false;
                sprite_shirt.visible = true;
                sprite_shirt.setInteractive();

                fxBag = this.sound.add('mp3bag');
                fxBag.play();         

            }, this);

            sprite_poloB.on('pointerdown', function (pointer, gameObject) {

                poloBPacked = true;
                sprite_poloB.visible = false;
                sprite_poloB.disableInteractive();

                poloGPacked = false;
                sprite_poloG.visible = true;
                sprite_poloG.setInteractive();

                poloRPacked = false;
                sprite_poloR.visible = true;
                sprite_poloR.setInteractive();

                shirtPacked = false;
                sprite_shirt.visible = true;
                sprite_shirt.setInteractive();

                fxBag = this.sound.add('mp3bag');
                fxBag.play();         

            }, this);

            sprite_shirt.on('pointerdown', function (pointer, gameObject) {

                shirtPacked = true;
                sprite_shirt.visible = false;
                sprite_shirt.disableInteractive();

                poloGPacked = false;
                sprite_poloG.visible = true;
                sprite_poloG.setInteractive();

                poloRPacked = false;
                sprite_poloR.visible = true;
                sprite_poloR.setInteractive();

                poloBPacked = false;
                sprite_poloB.visible = true;
                sprite_poloB.setInteractive();


                fxBag = this.sound.add('mp3bag');
                fxBag.play();         

            }, this);
          
            sprite_books.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('BooksSceneL');
            }, this);

        }

        function createSportsbagScene()
        {

            var imgScene = this.add.image(0, 0, 'imgSportsbag').setOrigin(0);

            var sprite_mainRight = this.add.sprite(0, 0); 
            var sprite_sportsbag = this.add.sprite(0, 0);

            var plgn_mainRight = new Phaser.Geom.Polygon([      0, 0,       1920, 0,       1920, 1080,         0, 1080]);
            var plgn_sportsbag = new Phaser.Geom.Polygon([            330, 520,         990, 0,        1500, 0,     1580, 420,      1050, 1080,      520, 1080,      330, 730]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xaaeaee);
            //graphics.fillPoints(plgn_sportsbag.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainRight.setInteractive(plgn_mainRight, Phaser.Geom.Polygon.Contains);
            sprite_sportsbag.setInteractive(plgn_sportsbag, Phaser.Geom.Polygon.Contains);

            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {

                this.scene.start('MainSceneR');

            }, this);
            
           

            sprite_sportsbag.on('pointerdown', function (pointer, gameObject) {

                if (sportsbagOpen) {
                    var fxZip = this.sound.add('mp3zip');
                } else {
                    var fxZip = this.sound.add('mp3unzip');
                }
               
                fxZip.play();
                sportsbagOpen = !sportsbagOpen;

            }, this);

        }

        var tap = 0;
        function createTreadmillScene()
        {

            imgScene = this.add.image(0, 0, 'imgTreadmill').setOrigin(0);
            var imgReady = this.add.image(1050, 60, 'imgReady').setOrigin(0).setScale(0.2);
            var imgSteady = this.add.image(1050, 60, 'imgSteady').setOrigin(0).setScale(0.2);
            var imgGo = this.add.image(1050, 60, 'imgGo').setOrigin(0).setScale(0.2);
            var imgFaster = this.add.image(1050, 60, 'imgFaster').setOrigin(0).setScale(0.2);
            var imgGood = this.add.image(1050, 60, 'imgGood').setOrigin(0).setScale(0.2);

            imgReady.visible = false;
            imgSteady.visible = false;
            imgGo.visible = false;
            imgFaster.visible = false;
            imgGood.visible = false;


            

            var fxTreadmill = this.sound.add('mp3treadmill', { loop: 1, volume: 0.06 });
            var bgTreadmill = this.sound.add('mp3run');

            var fxStepL = this.sound.add('mp3stepL', {  volume: 0.25 });
            var fxStepR = this.sound.add('mp3stepR', { volume: 0.25 });
            var stepL = true;

            var sprite_mainRight = this.add.sprite(0, 0); 
            var sprite_treadmill = this.add.sprite(0, 0);
            var sprite_treadmillStart = this.add.sprite(0, 0); 
            var step = this.add.sprite(848, 955, 'imgStep').setOrigin().setScale(0.225);
            step.visible = false;

            var sprite_headBand = this.add.sprite(1115, 940, 'imgHeadbandScene7').setOrigin().setScale(1);

            if (headbandPacked) {
                sprite_headBand.visible = false;
                sprite_headBand.disableInteractive();
            } else {
                sprite_headBand.visible = true;
                sprite_headBand.setInteractive();
            }


            var plgn_mainRight = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_treadmillStart = new Phaser.Geom.Polygon([          630, 620,       1020, 620,       1020, 810,       630, 810]);
            var plgn_treadmill = new Phaser.Geom.Polygon([            450, 0,         1280, 0,        1280, 1080,      450, 1080]);

            //var graphics = this.add.graphics();
           
            //graphics.fillStyle(0xaaaaff);
            //graphics.fillPoints(plgn_treadmill.points, true);
            //graphics.fillStyle(0xaaeaee);
            //graphics.fillPoints(plgn_treadmillStart.points, true);

            text = this.add.text(500, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;
            
            sprite_mainRight.setInteractive(plgn_mainRight, Phaser.Geom.Polygon.Contains);
            sprite_treadmill.setInteractive(plgn_treadmill, Phaser.Geom.Polygon.Contains);
            sprite_treadmillStart.setInteractive(plgn_treadmillStart, Phaser.Geom.Polygon.Contains);


            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {

                this.scene.start('MainSceneR');
               
            }, this);

            step.on('pointerdown', function (pointer, gameObject) {
                tap += 10;
                step.visible = false;
                step.disableInteractive();
                if (stepL) {
                    fxStepL.play();
                } else {
                    fxStepR.play();
                }
                stepL = !stepL;

            }, this);

            sprite_headBand.on('pointerdown', function (pointer, gameObject) {

                sprite_headBand.disableInteractive();
                sprite_headBand.visible = false;
                headbandPacked = true;
                hatPacked = false;
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_treadmillStart.on('pointerdown', function (pointer, gameObject) {
                if (!treadmillRun) {
                    treadmillRun = true;
                    if (ambient.isPlaying) {
                        ambient.pause();
                    }
                    sprite_mainRight.disableInteractive();
                    //sprite_mainRight.stopPropagation();
                    var fxBttn = this.sound.add('mp3Bttn');
                    fxBttn.play();
                    //timerTreadmill = this.sys.game.loop.time;

                    timedEvent = this.time.addEvent({
                        delay: 1000, callback: () => {

                            fxTreadmill.play();

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 4000, callback: () => {

                            bgTreadmill.play();
                            imgReady.visible = true;

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 4487.80, callback: () => {

                            imgReady.visible = false;
                            imgSteady.visible = true;

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 4975.61, callback: () => {

                            imgSteady.visible = false;
                            imgGo.visible = true;
                           // step.visible = true;
                           // step.setInteractive();
                            timedEvent2 = this.time.addEvent({
                                delay: 487.80, callback: () => {
                                    if (!step.visible) {
                                        step.visible = true;
                                        step.setInteractive();
                                    }

                                }, callbackScope: this, repeat: 58, startAt: 0
                            });

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 5463.41, callback: () => {

                            
                            imgGo.visible = false;
                           

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });



                    timedEvent = this.time.addEvent({
                        delay: 18650, callback: () => {

                         
                            if (tap < 200) {
                                imgFaster.visible = true;
                            }
                            if (tap > 260) {
                                imgGood.visible = true;
                            }

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });


                    timedEvent = this.time.addEvent({
                        delay: 20650, callback: () => {

                            imgFaster.visible = false;
                            imgGood.visible = false;
                    
                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 34300, callback: () => {

                            imgFaster.visible = false;
                            imgGood.visible = false;
                            if (tap < 580) {
                                fxBreath = this.sound.add('mp3breath');
                                fxBreath.play();
                                tap = 0;
                            } else {
                                fxBreath = this.sound.add('mp3fanfair');
                                fxBreath.play();
                               
                                sprite_treadmillStart.disableInteractive();
                            }

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    
                    timedEvent = this.time.addEvent({
                        delay: 34740, callback: () =>  {

                           // imgGo.visible = false;
                            treadmillRun = false;
                            fxTreadmill.stop();
                            bgTreadmill.stop();
                            step.visible = false;
                            step.disableInteractive();
                            sprite_mainRight.setInteractive(plgn_mainRight, Phaser.Geom.Polygon.Contains);

                          

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 35000, callback: () =>  {

                           
                           
                           
                        }, callbackScope: this, repeat: 0, startAt: 0
                    });
                    
                }
                
            }, this);

        }
 
        function createBedScene()
        {

            imgScene = this.add.image(0, 0, 'imgBed').setOrigin(0);

            var sprite_mainRight = this.add.sprite(0, 0); 
            var sprite_bed = this.add.sprite(0, 0);
            var sprite_soundBox = this.add.sprite(0, 0);
            var sprite_books = this.add.sprite(0, 0); 
            var sprite_map = this.add.sprite(0, 0);
            var sprite_pants = this.add.sprite(1400, 740, 'imgPantsScene9').setOrigin(0).setInteractive();

            if (pantsPacked) {
                sprite_pants.visible = false;
                sprite_pants.disableInteractive();
            } else {
                sprite_pants.visible = true;
                sprite_pants.setInteractive();
            }

            var plgn_mainRight = new Phaser.Geom.Polygon([      0, 800,       720, 700,       1000, 1080,         0, 1080]);
            var plgn_bed = new Phaser.Geom.Polygon([            700, 320,       1300, 320,      1300, 470,      700, 550]);
            var plgn_soundBox = new Phaser.Geom.Polygon([       100, 300,       430, 330,      430, 530,       100, 480       ]);
            var plgn_books = new Phaser.Geom.Polygon([          230, 620,       420, 590,       430, 720,       230, 750]);
            var plgn_map = new Phaser.Geom.Polygon([            50, 0,         1000, 0,        1000, 150,      50, 150]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_mainRight.points, true);
            //graphics.fillStyle(0xaaaa00);
            //graphics.fillPoints(plgn_bed.points, true);
            //graphics.fillStyle(0xffaaff);
            //graphics.fillPoints(plgn_soundBox.points, true);
            //graphics.fillStyle(0xaaaaff);
            //graphics.fillPoints(plgn_books.points, true);
            //graphics.fillStyle(0xaaeaee);
            //graphics.fillPoints(plgn_map.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainRight.setInteractive(plgn_mainRight, Phaser.Geom.Polygon.Contains);
            sprite_bed.setInteractive(plgn_bed, Phaser.Geom.Polygon.Contains);
            sprite_soundBox.setInteractive(plgn_soundBox, Phaser.Geom.Polygon.Contains);
            sprite_books.setInteractive(plgn_books, Phaser.Geom.Polygon.Contains);
            sprite_map.setInteractive(plgn_map, Phaser.Geom.Polygon.Contains);

            sprite_pants.on('pointerdown', function (pointer, gameObject) {

                sprite_pants.disableInteractive();
                sprite_pants.visible = false;
                pantsPacked = true;
                fxBag = this.sound.add('mp3bag');
                fxBag.play();         

            }, this);

            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {

                this.scene.start('MainSceneR');

            }, this);
            
            sprite_bed.on('pointerdown', function (pointer, gameObject) {

                var fxYawn = this.sound.add('mp3yawn');
                fxYawn.play(); 

                this.cameras.main.fadeOut(3000);
                timedEvent = this.time.addEvent({
                    delay: 3250, callback: () => {

                        this.scene.start('MainScene0');

                    }, callbackScope: this, repeat: 0, startAt: 0
                    });

            }, this);

            sprite_soundBox.on('pointerdown', function (pointer, gameObject) {

                playAmbient();

            }, this);

            sprite_books.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('BooksSceneR');

            }, this);

            sprite_map.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('MapScene');

            }, this);

        }

        function createMapScene()
        {

            imgScene = this.add.image(0, 0, 'imgMap').setOrigin(0).setScale(1);
            this.add.image(466, 265, 'imgTrack1').setOrigin(0).setScale(1);
            //this.add.image(725, 472, 'imgTrack3').setOrigin(0).setScale(1);

            var sprite_mainRight = this.add.sprite(0, 0); 
            var sprite_map = this.add.sprite(0, 0); 
            var zoneMap = this.add.zone(0, 0).setOrigin(0);
            var zoneSlider4 = this.add.zone(0, 0).setOrigin(0);
            zoneMap.setName('zMap');
            zoneSlider4.setName('zSlider4');



            var sprite_flag1 = this.add.sprite(475, 330, 'imgFlag').setOrigin(0).setScale(0.075).setInteractive();
            var sprite_flag2 = this.add.sprite(828, 250, 'imgFlag').setOrigin(0).setScale(0.075).setInteractive();
            var sprite_flag3 = this.add.sprite(988, 335, 'imgFlag').setOrigin(0).setScale(0.075).setInteractive();
            var sprite_flag4 = this.add.sprite(560, 880, 'imgFlag').setOrigin(0).setScale(0.075).setInteractive();
          
            this.input.setDraggable(sprite_flag1);
            this.input.setDraggable(sprite_flag2);
            this.input.setDraggable(sprite_flag3);
            this.input.setDraggable(sprite_flag4);
          

            

            var plgn_mainRight = new Phaser.Geom.Polygon([      0, 0,       1920, 0,       1920, 1080,         0, 1080]);
            var plgn_map = new Phaser.Geom.Polygon([      180, 0,       1400, 120,       1400, 920,         180, 1080]);


            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_map.points, true);
           
            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainRight.setInteractive(plgn_mainRight, Phaser.Geom.Polygon.Contains);
            sprite_map.setInteractive(plgn_map, Phaser.Geom.Polygon.Contains);


            zoneMap.setInteractive(plgn_map, Phaser.Geom.Polygon.Contains);
           // zoneSlider4.setInteractive(plgnSlider4, Phaser.Geom.Polygon.Contains);
            zoneMap.input.dropZone = true;
            //zoneSlider4.input.dropZone = true;

           

            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {
                this.scene.start('MainSceneR');
            }, this);
            
            this.input.on('drag', function (pointer, gameObject, dragX, dragY) {

                if (dragX > 200 && dragX < 1400) {
                    gameObject.x = dragX;
                }
                
                gameObject.y = dragY;

                gameObject.setScale(0.075 - (3.63/190000) * gameObject.x);
            });
        }

        function createBoardScene() {

            var imgScene = this.add.image(0, 0, 'imgBoard').setOrigin(0);

            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_board = this.add.sprite(0, 0);

            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_board = new Phaser.Geom.Polygon([290, 0, 1690, 0, 1650, 860, 330, 860]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_map.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_board.setInteractive(plgn_board, Phaser.Geom.Polygon.Contains);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('MainSceneL');
            }, this);


        }

        function createShelfScene() {

            var imgScene = this.add.image(0, 0, 'imgShelf').setOrigin(0);

            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_shelf = this.add.sprite(0, 0);

            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_shelf = new Phaser.Geom.Polygon([480, 340, 1520, 340, 1520, 850, 480, 850]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
      //      graphics.fillPoints(plgn_shelf.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_shelf.setInteractive(plgn_shelf, Phaser.Geom.Polygon.Contains);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('MainSceneL');
            }, this);


        }

        function createLaptopScene() {

            var imgScene = this.add.image(0, 0, 'imgLaptop').setOrigin(0);

            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_laptop = this.add.sprite(0, 0);

            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_laptop = new Phaser.Geom.Polygon([320, 100, 1650, 100, 1650, 920, 320, 920]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_map.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_laptop.setInteractive(plgn_laptop, Phaser.Geom.Polygon.Contains);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('MainSceneL');
            }, this);


        }

        function createDeskScene() {

            imgSceneClosed = this.add.image(0, 0, 'imgDeskClosed').setOrigin(0);
           
            var groupMonth = this.add.group();
            for (var i = 1; i <= 12; i++) {
                groupMonth.create(784, 309, 'imgM' + i).setOrigin(0);
            }
            var childMonth = groupMonth.getChildren();
            for (var i = 0; i < 12; i++) {
                childMonth[i].visible = false;
            }
            childMonth[g_month].visible = true;

            var groupDayH = this.add.group();
            for (var i = 0; i <= 3; i++) {
                groupDayH.create(823, 318, 'imgD' + i).setOrigin(0);
            }
            var childDayH = groupDayH.getChildren();
            for (var i = 0; i < 4; i++) {
                childDayH[i].visible = false;
            }

            childDayH[g_dayH].visible = true;

            var groupDayL = this.add.group();
            for (var i = 0; i <= 9; i++) {
                groupDayL.create(861, 326, 'imgD' + i).setOrigin(0);
            }
            var childDayL = groupDayL.getChildren();
            for (var i = 0; i < 10; i++) {
                childDayL[i].visible = false;
            }
            childDayL[g_dayL].visible = true;



            var imgSceneOpened = this.add.image(101, 700, 'imgDeskOpened').setOrigin(0);
            imgSceneOpened.visible = false;
           
            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_board = this.add.sprite(0, 0);
            var sprite_shelf = this.add.sprite(0, 0);
            var sprite_laptop = this.add.sprite(0, 0);

            var sprite_month = this.add.sprite(0, 0);
            var sprite_dayH = this.add.sprite(0, 0);
            var sprite_dayL = this.add.sprite(0, 0);

            var sprite_book = this.add.sprite(520, 715, 'imgBook').setOrigin(0).setScale(1.2);
            var sprite_clock = this.add.sprite(450, 745, 'imgClock').setOrigin(0);
            var sprite_tracker = this.add.sprite(325, 810, 'imgTracker').setOrigin(0);
            sprite_book.visible = false;
            sprite_clock.visible = false;
            sprite_tracker.visible = false;


            var plgn_mainLeft = new Phaser.Geom.Polygon([830, 710, 1920, 670, 1920, 1080, 830, 1080]);
            var plgn_board = new Phaser.Geom.Polygon([250, 0, 1920, 0, 1920, 100, 250, 120]);
            var plgn_shelf = new Phaser.Geom.Polygon([100, 730, 770, 700, 770, 1080, 100, 1080]);
            var plgn_laptop = new Phaser.Geom.Polygon([860, 210, 1200, 130, 1360, 490, 1020, 600]);

            var plgn_month = new Phaser.Geom.Polygon([770, 285, 815, 295, 815, 350, 770, 340]);
            var plgn_dayH = new Phaser.Geom.Polygon([815, 295, 860, 305, 860, 360, 815, 350]);
            var plgn_dayL = new Phaser.Geom.Polygon([860, 305, 905, 315, 905, 370, 860, 360]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_month.points, true);

           
            //graphics.fillStyle(0xffaaff);
            //graphics.fillPoints(plgn_dayH.points, true);

            //graphics.fillStyle(0xaaaa00);
            //graphics.fillPoints(plgn_dayL.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_board.setInteractive(plgn_board, Phaser.Geom.Polygon.Contains);
            sprite_shelf.setInteractive(plgn_shelf, Phaser.Geom.Polygon.Contains);
            sprite_laptop.setInteractive(plgn_laptop, Phaser.Geom.Polygon.Contains);

            sprite_month.setInteractive(plgn_month, Phaser.Geom.Polygon.Contains);
            sprite_dayH.setInteractive(plgn_dayH, Phaser.Geom.Polygon.Contains);
            sprite_dayL.setInteractive(plgn_dayL, Phaser.Geom.Polygon.Contains);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('MainSceneL');
            }, this);

            sprite_board.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('BoardScene');
            }, this);

            sprite_shelf.on('pointerdown', function (pointer, gameObject) {

                
                if (shelfOpen) {
                    this.sound.play('mp3drawerClose');

                    imgSceneOpened.visible = false;
                    sprite_tracker.visible = false;
                    sprite_clock.visible = false;
                    sprite_book.visible = false;

                    sprite_book.disableInteractive();
                    sprite_clock.disableInteractive();
                    sprite_tracker.disableInteractive();


                } else {

                    this.sound.play('mp3drawerOpen');

                    if (!clockPacked) {
                        sprite_clock.visible = true;
                        sprite_clock.setInteractive();
                    }
                    if (!trackerPacked) {
                        sprite_tracker.visible = true;
                        sprite_tracker.setInteractive();
                    }

                    sprite_book.visible = true;
                    sprite_book.setInteractive();


                    imgSceneOpened.visible = true;
                    
                }

                shelfOpen = !shelfOpen;

            }, this);

            sprite_laptop.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('LaptopScene');
            }, this);

            sprite_book.on('pointerdown', function (pointer, gameObject) {


            }, this);

            sprite_clock.on('pointerdown', function (pointer, gameObject) {

                sprite_clock.disableInteractive();
                sprite_clock.visible = false;
                clockPacked = true;
                armbandPacked = false;
                trackerPacked = false;
                sprite_tracker.visible = true;
                sprite_tracker.setInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_tracker.on('pointerdown', function (pointer, gameObject) {

                sprite_tracker.disableInteractive();
                sprite_tracker.visible = false;
                trackerPacked = true;
                armbandPacked = false;
                clockPacked = false;
                sprite_clock.visible = true;
                sprite_clock.setInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_month.on('pointerdown', function (pointer, gameObject) {

                g_month++;
                if (g_month > 11) {
                    g_month = 0;
                }
                for (var i = 0; i < 12; i++) {
                    childMonth[i].visible = false;
                }
                childMonth[g_month].visible = true;

            }, this);

            sprite_dayH.on('pointerdown', function (pointer, gameObject) {

                g_dayH++;
                if (g_dayH > 3) {
                    g_dayH = 0;
                }
                for (var i = 0; i < 4; i++) {
                    childDayH[i].visible = false;
                }
                childDayH[g_dayH].visible = true;

            }, this);

            sprite_dayL.on('pointerdown', function (pointer, gameObject) {

                g_dayL++;
                if (g_dayL > 9) {
                    g_dayL = 0;
                }
                for (var i = 0; i < 10; i++) {
                    childDayL[i].visible = false;
                }
                childDayL[g_dayL].visible = true;

            }, this);

        }




 
        function updateMainScene0()
        { 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown()
            ]);
        }

        function updateMainSceneL()
        { 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown()
            ]);
        }

        function updateMainSceneR()
        { 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown()
            ]);
        }

        function updateWardrobeScene()
        { 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown()
            ]);
        }

        function updateSportsbagScene()
        { 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown()
            ]);
        }

        function updateTreadmillScene()
        { 
 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown(),
                'tap: ' + tap
            ]);
            
            
        }

        function updateBedScene()
        { 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown()
            ]);
        }

        function updateMapScene()
        { 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown()
            ]);
        }

        function updateBoardScene()
        { 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown()
            ]);
        }

        function updateShelfScene()
        { 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown()
            ]);
        }

        function updateLaptopScene()
        { 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown()
            ]);
        }

        function updateDeskScene()
        { 
            var pointer = this.input.activePointer;
            text.setText([
                'x: ' + pointer.worldX,
                'y: ' + pointer.worldY,
                'isDown: ' + pointer.isDown,
                'rightButtonDown: ' + pointer.rightButtonDown()
            ]);
        }

        function updateControl() {       
            var pointer = this.input.activePointer;
        }

        function playAmbient() {
            click.play();
            if (ambient.isPlaying) {
                ambient.pause();
            } else {
                if (ambientOn) {
                    ambient.resume();
                } else {
                    ambientOn = true;
                    ambient.play();
                }
            }
        }

 


    </script>

</body>
</html>
