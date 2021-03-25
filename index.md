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
 

            
            this.load.image('imgReady', 'assets/sprites/ready.png');
            this.load.image('imgSteady', 'assets/sprites/steady.png');
            this.load.image('imgGo', 'assets/sprites/go.png');
            this.load.image('imgFaster', 'assets/sprites/faster.png');
            this.load.image('imgGood', 'assets/sprites/good.png');
            this.load.image('imgStep', 'assets/sprites/run3.png');
   
            this.load.audio('mp3stepL', 'assets/sound/stepL.mp3');
            this.load.audio('mp3stepR', 'assets/sound/stepR.mp3');
            this.load.audio('mp3breath', 'assets/sound/breath.mp3');
            this.load.audio('mp3fanfair', 'assets/sound/fanfair.mp3');

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
            this.load.image('imgDeskOpened', 'assets/background/scene2.2.jpg');
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
  
        var ambient;    
        var cick;    
        var ambientOn = false;    
        var shelfWin = true;    
        var sportsbagOpen = true;    
        var wardrobeOpen = false;    
        var headBandPacked = false;    
        var treadmillRun = false;
        var timerTreadmill;


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

            var imgScene = this.add.image(0, 0, 'imgWakeUp').setOrigin(0);
            this.cameras.main.fadeIn(6000);

            var fxCock = this.sound.add('mp3cock');
            fxCock.play(); 
        
            var sprite_mainLeft = this.add.sprite(0, 0); 
            var sprite_mainRight = this.add.sprite(0, 0); 
            var sprite_wardrobe = this.add.sprite(0, 0); 
            var sprite_soundBox = this.add.sprite(0, 0);
       
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

            if (!headBandPacked) {
                var sprite_headBand = this.add.sprite(1460, 910, 'imgPinUnconnected').setOrigin().setScale(1).setInteractive();
                this.input.setDraggable(sprite_headBand);
            }

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('MainSceneL');

            },this);

            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('MainSceneR');

           },this);

            sprite_wardrobe.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('WardrobeScene');

            },this);

            sprite_soundBox.on('pointerdown', function (pointer, gameObject) {
                playAmbient();
            }, this);

            sprite_headBand.on('pointerdown', function (pointer, gameObject) {
                headBandPacked = true;
                sprite_headBand.visible = false;
            },this);

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

                this.scene.switch('MainSceneR');

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

            var imgScene = this.add.image(0, 0, 'imgMainSceneRight').setOrigin(0);

            var sprite_treadmill = this.add.sprite(0, 0); 
            var sprite_wardrobe = this.add.sprite(0, 0); 
            var sprite_mainLeft = this.add.sprite(0, 0); 
            var sprite_sportsBag = this.add.sprite(0, 0); 
            var sprite_soundBox = this.add.sprite(0, 0); 
            var sprite_books = this.add.sprite(0, 0); 
            var sprite_bed = this.add.sprite(0, 0); 
            var sprite_map = this.add.sprite(0, 0); 
        
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

                this.scene.switch('BooksSceneR');

            }, this);

            sprite_bed.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('BedScene');

            }, this);

            sprite_map.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('MapScene');

            }, this);


            // sprite_headBand.on('pointerdown', function (pointer, gameObject) {
           //     headBandPacked = true;
           //     sprite_headBand.visible = false;
           // },this);

    }

        function createWardrobeScene()
        {

            var imgScene = this.add.image(0, 0, 'imgWardrobe').setOrigin(0);

            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_mainRight = this.add.sprite(0, 0);
            var sprite_wardrobe = this.add.sprite(0, 0);
            var sprite_books = this.add.sprite(0, 0);

            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 500, 0, 500, 1080, 0, 1080]);
            var plgn_mainRight = new Phaser.Geom.Polygon([1350, 0, 1920, 0, 1920, 1080, 1350, 1080]);
            var plgn_wardrobe = new Phaser.Geom.Polygon([500, 0, 1350, 0, 1350, 1080, 500, 1080]);
            var plgn_books = new Phaser.Geom.Polygon([360, 100, 520, 100, 520, 260, 360, 260]);

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

                this.scene.switch('MainSceneL');

            }, this);
            
           sprite_mainRight.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('MainSceneR');

            }, this);
            
           

            sprite_wardrobe.on('pointerdown', function (pointer, gameObject) {

                if (wardrobeOpen) {
                    var fxWardrobe = this.sound.add('mp3wClose');
                } else {
                    var fxWardrobe = this.sound.add('mp3wOpen');
                }
               
                fxWardrobe.play();
                wardrobeOpen = !wardrobeOpen;

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

                this.scene.switch('MainSceneR');

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
            var step = this.add.sprite(850, 950, 'imgStep').setOrigin().setScale(0.225);
            step.visible = false;
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

                this.scene.switch('MainSceneR');
               
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

            var imgScene = this.add.image(0, 0, 'imgBed').setOrigin(0);

            var sprite_mainRight = this.add.sprite(0, 0); 
            var sprite_bed = this.add.sprite(0, 0);
            var sprite_soundBox = this.add.sprite(0, 0);
            var sprite_books = this.add.sprite(0, 0); 
            var sprite_map = this.add.sprite(0, 0);

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


            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('MainSceneR');

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

            var imgScene = this.add.image(0, 0, 'imgMap').setOrigin(0);

            var sprite_mainRight = this.add.sprite(0, 0); 
            var sprite_map = this.add.sprite(0, 0); 
         
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
       
            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('MainSceneR');
            }, this);
            

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

            var imgSceneClosed = this.add.image(0, 0, 'imgDeskClosed').setOrigin(0);
            var imgSceneOpened = this.add.image(0, 0, 'imgDeskOpened').setOrigin(0);
            imgSceneOpened.visible = false;


            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_board = this.add.sprite(0, 0);
            var sprite_shelf = this.add.sprite(0, 0);
            var sprite_laptop = this.add.sprite(0, 0);

            var plgn_mainLeft = new Phaser.Geom.Polygon([830, 710, 1920, 670, 1920, 1080, 830, 1080]);
            var plgn_board = new Phaser.Geom.Polygon([250, 0, 1920, 0, 1920, 100, 250, 120]);
            var plgn_shelf = new Phaser.Geom.Polygon([100, 730, 770, 700, 770, 1080, 100, 1080]);
            var plgn_laptop = new Phaser.Geom.Polygon([860, 210, 1200, 130, 1360, 490, 1020, 600]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_board.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_board.setInteractive(plgn_board, Phaser.Geom.Polygon.Contains);
            sprite_shelf.setInteractive(plgn_shelf, Phaser.Geom.Polygon.Contains);
            sprite_laptop.setInteractive(plgn_laptop, Phaser.Geom.Polygon.Contains);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('MainSceneL');
            }, this);

            sprite_board.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('BoardScene');
            }, this);

            sprite_shelf.on('pointerdown', function (pointer, gameObject) {

                if (!shelfWin) {
                    this.scene.switch('ShelfeScene');
                } else {
                    if (!imgSceneOpened.visible) {
                        this.sound.play('mp3drawerOpen');
                        imgSceneClosed.visible = false;
                        imgSceneOpened.visible = true;
                    } else {
                        this.sound.play('mp3drawerClose');
                        imgSceneClosed.visible = true;
                        imgSceneOpened.visible = false;
                    }
                   
                    
                }

               
           
                

            }, this);
            sprite_laptop.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('LaptopScene');
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
