<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width">
    <script src='src/phaser-arcade-physics.min.js'></script>
</head>
<body>

    <script>

        var Preloader = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function Preloader() {
                    Phaser.Scene.call(this, 'preloader');
                },

            preload: function () {




                var width = this.cameras.main.width;
                var height = this.cameras.main.height;
                var loadingText = this.make.text({
                    x: width / 2 - 110,
                    y: height / 2 - 50,
                    text: 'Loading',
                    style: {
                        font: '60px monospace',
                        fill: '#000000'
                    }
                });
                loadingText.setOrigin(0.5, 0.5);

                var percentText = this.make.text({
                    x: width / 2 + 100,
                    y: height / 2 - 50,
                    text: '0%',
                    style: {
                        font: '60px monospace',
                        fill: '#000000'
                    }
                });
                percentText.setOrigin(0.5, 0.5);

                var assetText = this.make.text({
                    x: width / 2,
                    y: height / 2 + 50,
                    text: '',
                    style: {
                        font: '12px monospace',
                        fill: '#fff00f'
                    }
                });

                assetText.setOrigin(0.5, 0.5);

                this.load.on('progress', function (value) {
                    percentText.setText(parseInt(value * 100) + '%');

                });

                this.load.on('fileprogress', function (file) {
                    assetText.setText('Loading asset: ' + file.key);
                });

                this.load.on('complete', function () {

                    loadingText.destroy();
                    percentText.destroy();
                    assetText.destroy();
                });


                this.load.image('imgStartBG', 'assets/background/start.jpg');

                this.load.image('imgM_bg', 'assets/marathon/background.jpg');
                this.load.image('imgM_mounts', 'assets/marathon/mounts.png');
                this.load.image('imgM_forest', 'assets/marathon/forest.png');
                this.load.image('imgM_sky1', 'assets/marathon/sky1.png');
                this.load.image('imgM_sky2', 'assets/marathon/sky2.png');
                this.load.image('imgM_front1', 'assets/marathon/front1.png');
                this.load.image('imgM_front2', 'assets/marathon/front2.png');
                this.load.image('imgM_grass', 'assets/marathon/grass.png');
                this.load.image('imgM_grass0', 'assets/marathon/grass0.png');
                this.load.image('imgM_road', 'assets/marathon/road.png');
                this.load.image('imgM_start', 'assets/marathon/start.png');
                this.load.image('imgM_finish', 'assets/marathon/finish.png');

                for (var i = 1; i <= 8; i++) {
                    this.load.image('imgM_b' + i, 'assets/marathon/mid/b' + i + '.png');
                }

                for (var i = 1; i <= 8; i++) {
                    this.load.image('imgM_b' + i, 'assets/marathon/mid/b' + i + '.png');
                }

                for (var i = 1; i <= 6; i++) {
                    this.load.image('imgM_R0_' + i, 'assets/marathon/run0/' + i + '.png');
                }

                for (var i = 1; i <= 6; i++) {
                    this.load.image('imgM_R1_' + i, 'assets/marathon/run1/' + i + '.png');
                }

                for (var i = 1; i <= 6; i++) {
                    this.load.image('imgM_R2_' + i, 'assets/marathon/run2/' + i + '.png');
                }

                for (var i = 1; i <= 6; i++) {
                    this.load.image('imgM_R3_' + i, 'assets/marathon/run3/' + i + '.png');
                }

                for (var i = 1; i <= 6; i++) {
                    this.load.image('imgM_R4_' + i, 'assets/marathon/run4/' + i + '.png');
                }

                for (var i = 1; i <= 6; i++) {
                    this.load.image('imgM_R5_' + i, 'assets/marathon/run5/' + i + '.png');
                }

                for (var i = 1; i <= 6; i++) {
                    this.load.image('imgM_R6_' + i, 'assets/marathon/run6/' + i + '.png');
                }

                for (var i = 1; i <= 6; i++) {
                    this.load.image('imgM_R7_' + i, 'assets/marathon/run7/' + i + '.png');
                }

                for (var i = 1; i <= 6; i++) {
                    this.load.image('imgM_R8_' + i, 'assets/marathon/run8/' + i + '.png');
                }


                for (var i = 1; i <= 7; i++) {
                    this.load.image('imgMag' + i, 'assets/books/m' + i + '.png');
                }







                this.load.html('nameform', 'assets/text/nameform.html');

                this.load.image('imgHeadbandMain0', 'assets/sprites/headbandMain0.png');
                this.load.image('imgHeadbandMain2', 'assets/sprites/headbandMain2.png');
                this.load.image('imgHeadbandScene7', 'assets/sprites/headbandScene7.png');
                this.load.image('imgHeadbandScene6', 'assets/sprites/headbandScene6.png');
                this.load.image('imgDeskOpened', 'assets/sprites/shelf.png');
                this.load.image('imgBook', 'assets/sprites/book.png');
                this.load.image('imgClock', 'assets/sprites/clock.png');
                this.load.image('imgTracker', 'assets/sprites/tracker.png');
                this.load.image('imgMagazine', 'assets/sprites/magazine.png');

                this.load.image('imgListPart1', 'assets/sprites/listPart1.png');
                this.load.image('imgListPart2', 'assets/sprites/listPart2.png');
                this.load.image('imgListPart3', 'assets/sprites/listPart3.png');

                this.load.image('imgNote1', 'assets/sprites/notes1Scene2.png');
                this.load.image('imgNote2', 'assets/sprites/notes2Scene2.png');
                this.load.image('imgNote3', 'assets/sprites/notes3Scene2.png');
                this.load.image('imgNote4', 'assets/sprites/notes4Scene2.png');

                this.load.image('imgHint', 'assets/sprites/hint.png');
                this.load.image('imgHintL', 'assets/sprites/hintL.png');


                for (var i = 1; i <= 12; i++) {
                    this.load.image('imgM' + i, 'assets/sprites/calendar/m' + i + '.png');
                }
                for (var i = 0; i <= 9; i++) {
                    this.load.image('imgD' + i, 'assets/sprites/calendar/' + i + '.png');
                }

                for (var i = 1; i <= 12; i++) {
                    this.load.image('imgCountry' + i, 'assets/sprites/opponents/c' + i + '.png');
                }
                for (var i = 1; i <= 4; i++) {
                    this.load.image('imgList' + i, 'assets/sprites/opponents/l' + i + '.png');
                }

                this.load.image('imgListFull', 'assets/sprites/opponents/lFull.png');

                this.load.image('imgBNG', 'assets/sprites/board/bng.jpg');
                this.load.image('imgPoster', 'assets/sprites/board/poster.png');
                this.load.image('imgCheck', 'assets/sprites/board/check.png');
                this.load.image('imgChecklist', 'assets/sprites/board/checklist.png');
                this.load.image('imgChecklistW', 'assets/sprites/board/checklistW.png');
                this.load.image('imgBoardFlag1', 'assets/sprites/board/flag1.png');
                this.load.image('imgBoardFlag2', 'assets/sprites/board/flag2.png');
                this.load.image('imgBall', 'assets/sprites/board/ball.png');
                this.load.image('imgSticker', 'assets/sprites/board/sticker.png');
                this.load.image('imgLamp', 'assets/sprites/board/lamp.png');


                for (var i = 1; i <= 5; i++) {
                    this.load.image('imgBoardRun' + i, 'assets/sprites/board/run' + i + '.png');
                }

                this.load.image('imgBttnOn', 'assets/sprites/shelf/bttnOn.png');
                this.load.image('imgBttnOff', 'assets/sprites/shelf/bttnOff.png');

                for (var i = 0; i <= 9; i++) {
                    this.load.image('imgShelfD' + i, 'assets/sprites/shelf/' + i + '.png');
                }

                this.load.image('imgLaptop1Scene2', 'assets/sprites/laptop1Scene2.png');
                this.load.image('imgLaptop2Scene2', 'assets/sprites/laptop2Scene2.png');
                this.load.image('imgLaptop1Scene3', 'assets/sprites/laptop/desktop1.png');
                this.load.image('imgLaptop2Scene3', 'assets/sprites/laptop/desktop2.png');

                this.load.image('imgLaptopFlag', 'assets/sprites/laptop/flagMain.png');
                this.load.image('imgLaptopFlag1', 'assets/sprites/laptop/flag1.png');
                this.load.image('imgLaptopFlag2', 'assets/sprites/laptop/flag2.png');
                this.load.image('imgLaptopFlag3', 'assets/sprites/laptop/flag3.png');
                this.load.image('imgLaptopFlag3.1', 'assets/sprites/laptop/flag3.1.png');
                this.load.image('imgLaptopFlag4', 'assets/sprites/laptop/flag4.png');
                this.load.image('imgLaptopFlag5', 'assets/sprites/laptop/flag5.png');
                this.load.image('imgLaptopFlag6', 'assets/sprites/laptop/flag6.png');
                this.load.image('imgLaptopFlag7', 'assets/sprites/laptop/flag7.png');

                this.load.image('imgPowerScene3', 'assets/sprites/laptop/power.png');
                this.load.image('imgLockScene3', 'assets/sprites/laptop/lock.png');
                this.load.image('imgPrinterScene3', 'assets/sprites/laptop/printer.png');
                this.load.image('imgPrinterMessageScene3', 'assets/sprites/laptop/printerMessage.png');
                this.load.image('imgPrinterOk', 'assets/sprites/laptop/ok.png');
                this.load.image('imgPrinterL', 'assets/sprites/laptop/left.png');
                this.load.image('imgPrinterR', 'assets/sprites/laptop/right.png');
                this.load.image('imgFileMessageScene3', 'assets/sprites/laptop/fileMessage.png');

                this.load.image('imgPrinterGreen', 'assets/sprites/printerGreen.png');
                this.load.image('imgPrinterRed', 'assets/sprites/printerRed.png');
                this.load.image('imgSheet', 'assets/sprites/sheet.png');
                this.load.image('imgPrinterClear', 'assets/sprites/printerClear.png');
                this.load.image('imgPrinterPrinted', 'assets/sprites/printerPrinted.png');

                this.load.image('imgBNGScene5', 'assets/sprites/bngScene5.png');
                this.load.image('imgListFScene5', 'assets/sprites/lFullScene5.png');
                this.load.image('imgListScene5', 'assets/sprites/listScene5.png');
                this.load.image('imgBallScene5', 'assets/sprites/ballScene5.png');
                this.load.image('imgBoardScene5', 'assets/sprites/boardScene5.png');
                this.load.image('imgWardrobeScene5', 'assets/sprites/wardrobeScene5.png');
                this.load.image('imgWardrobeSceneMain2', 'assets/sprites/wardrobeSceneMain2.png');
                this.load.image('imgShirtScene5', 'assets/sprites/shirtScene5.png');
                this.load.image('imgShirtScene6', 'assets/sprites/shirtScene6.png');
                this.load.image('imgShoesRScene5', 'assets/sprites/shoesRScene5.png');
                this.load.image('imgShoesWScene5', 'assets/sprites/shoesWScene5.png');
                this.load.image('imgShoesRScene6', 'assets/sprites/shoesRScene6.png');
                this.load.image('imgShoesWScene6', 'assets/sprites/shoesWScene6.png');
                this.load.image('imgPoloGScene5', 'assets/sprites/poloGScene5.png');
                this.load.image('imgPoloRScene5', 'assets/sprites/poloRScene5.png');
                this.load.image('imgPoloBScene5', 'assets/sprites/poloBScene5.png');
                this.load.image('imgPoloGScene6', 'assets/sprites/poloGScene6.png');
                this.load.image('imgPoloRScene6', 'assets/sprites/poloRScene6.png');
                this.load.image('imgPoloBScene6', 'assets/sprites/poloBScene6.png');
                this.load.image('imgHatScene5', 'assets/sprites/hatScene5.png');
                this.load.image('imgHatScene6', 'assets/sprites/hatScene6.png');
                this.load.image('imgArmbandScene6', 'assets/sprites/armbandScene6.png');

                this.load.image('imgBagClose', 'assets/sprites/bagCapClose.png');
                this.load.image('imgBagOpen', 'assets/sprites/bagCapOpen.png');
                this.load.image('imgBagOpenMain0', 'assets/sprites/bagOpenMain0.png');
                this.load.image('imgBagOpenMain2', 'assets/sprites/bagOpenMain2.png');

                for (var i = 0; i <= 9; i++) {
                    this.load.image('imgTreadmillD' + i, 'assets/sprites/treadmill/' + i + '.png');
                }

                this.load.image('imgReady', 'assets/sprites/ready.png');
                this.load.image('imgSteady', 'assets/sprites/steady.png');
                this.load.image('imgGo', 'assets/sprites/go.png');
                this.load.image('imgFaster', 'assets/sprites/faster.png');
                this.load.image('imgGood', 'assets/sprites/good.png');
                this.load.image('imgFail', 'assets/sprites/fail.png');
                this.load.image('imgStep', 'assets/sprites/run3.png');
                this.load.image('imgPB', 'assets/sprites/treadmill/PB.png');

                this.load.image('imgFlag', 'assets/sprites/flagScene8.png');
                this.load.image('imgFlag2', 'assets/sprites/flagMainScene2.png');
                this.load.image('imgTrack1', 'assets/sprites/track1.png');

                this.load.image('imgPantsSceneMain2', 'assets/sprites/pantsSceneMain2.png');
                this.load.image('imgPantsScene9', 'assets/sprites/pantsScene9.png');
                this.load.image('imgPantsScene6', 'assets/sprites/pantsScene6.png');

                this.load.audio('mp3stepL', 'assets/sound/stepL.mp3');
                this.load.audio('mp3stepR', 'assets/sound/stepR.mp3');
                this.load.audio('mp3breath', 'assets/sound/breath.mp3');
                this.load.audio('mp3fanfair', 'assets/sound/fanfair.mp3');

                this.load.audio('mp3print', 'assets/sound/printer.mp3');
                this.load.audio('mp3shelfBttn', 'assets/sound/swOn.mp3');
                this.load.audio('mp3page', 'assets/sound/page.mp3');
                this.load.audio('mp3bag', 'assets/sound/bag.mp3');
                this.load.audio('mp3drawerClose', 'assets/sound/drawerClose.mp3');
                this.load.audio('mp3drawerOpen', 'assets/sound/drawerOpen.mp3');
                this.load.audio('mp3Bttn', 'assets/sound/bttn.mp3');
                this.load.audio('mp3cock', 'assets/sound/cock.mp3');
                this.load.audio('mp3shoot', 'assets/sound/shoot.mp3');

                this.load.audio('mp3Calendar', 'assets/sound/calendar.mp3');
                this.load.audio('mp3Sheet', 'assets/sound/sheet.mp3');
                this.load.audio('mp3Flag', 'assets/sound/flag.mp3');
                this.load.audio('mp3Mark1', 'assets/sound/mark1.mp3');
                this.load.audio('mp3Mark2', 'assets/sound/mark2.mp3');
                this.load.audio('mp3Mark3', 'assets/sound/mark3.mp3');
                this.load.audio('mp3Laptop', 'assets/sound/laptopOn.mp3');
                this.load.audio('mp3Laptop2', 'assets/sound/laptopOn2.mp3');
                this.load.audio('mp3Laptop3', 'assets/sound/laptopOn3.mp3');
                this.load.audio('mp3AppBttn', 'assets/sound/wBttn.mp3');
                this.load.audio('mp3Unlock', 'assets/sound/unlock.mp3');
                this.load.audio('mp3SoundBttn', 'assets/sound/soundBttn.mp3');
                this.load.audio('mp3yawn', 'assets/sound/yawn.mp3');
                this.load.audio('mp3zip', 'assets/sound/zip.mp3');
                this.load.audio('mp3unzip', 'assets/sound/unzip.mp3');
                this.load.audio('mp3wOpen', 'assets/sound/wardrobeOpen.mp3');
                this.load.audio('mp3wClose', 'assets/sound/wardrobeClose.mp3');
                this.load.audio('mp3Final', 'assets/sound/final.mp3');

                this.load.audio('mp3ambient', 'assets/ambient/Ketsa.mp3');
                this.load.audio('mp3run', 'assets/ambient/run.mp3');
                this.load.audio('mp3treadmill', 'assets/ambient/treadmill.mp3');
                this.load.audio('mp3marathon', 'assets/ambient/marathon.mp3');

                this.load.image('book1.0', 'assets/books/1.0.png');
                this.load.image('book1.1', 'assets/books/1.1.png');
                this.load.image('book1.2', 'assets/books/1.2.png');
                this.load.image('book2.0', 'assets/books/2.0.png');
                this.load.image('book2.1', 'assets/books/2.1.png');
                this.load.image('book3.0', 'assets/books/3.0.png');
                this.load.image('book3.1', 'assets/books/3.1.png');
                this.load.image('book3.2', 'assets/books/3.2.png');

                this.load.image('imgWakeUp', 'assets/background/sceneMain0.jpg');
                this.load.image('imgMainSceneRight', 'assets/background/sceneMain2.jpg');
                this.load.image('imgBoard', 'assets/background/scene1.jpg');
                this.load.image('imgDeskClosed', 'assets/background/scene2.jpg');
                this.load.image('imgDeskClosedB', 'assets/background/scene2b.jpg');
                this.load.image('imgLaptop', 'assets/background/scene3.jpg');
                this.load.image('imgShelf', 'assets/background/scene4.jpg');
                this.load.image('imgWardrobe', 'assets/background/scene5.jpg');
                this.load.image('imgSportsbag', 'assets/background/scene6.jpg');
                this.load.image('imgSportsbagL', 'assets/background/scene6L.png');
                this.load.image('imgTreadmill', 'assets/background/scene7.jpg');
                this.load.image('imgMap', 'assets/background/scene8.jpg');
                this.load.image('imgBed', 'assets/background/scene9.jpg');
                this.load.image('imgFinal', 'assets/background/final.jpg');

            },

            create: function () {
                //imgStartScene = this.add.image(0, 0, 'imgLoading').setOrigin(0);
                this.scene.start('StartScene');
                ambient = this.sound.add('mp3ambient', { loop: 1, volume: 0.05 });
                click = this.sound.add('mp3SoundBttn', { volume: 2 });
            }


        });

        var FinalScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function FinalScene() {
                    Phaser.Scene.call(this, { key: 'FinalScene', active: false });
                },
            create: createFinalScene

        });

        var StartScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function StartScene() {
                    Phaser.Scene.call(this, { key: 'StartScene', active: true });
                },
            create: createStartScene

        });

        var MainScene0 = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function MainScene0() {
                    Phaser.Scene.call(this, { key: 'MainScene0', active: false });
                },
            preload: preloadMainScene0,
            create: createMainScene0,
            update: updateMainScene0

        });

        var MainSceneR = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function MainSceneR() {
                    Phaser.Scene.call(this, { key: 'MainSceneR', active: false });
                },
            preload: preloadMainSceneR,
            create: createMainSceneR,
            update: updateMainSceneR

        });

        var WardrobeScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function WardrobeScene() {
                    Phaser.Scene.call(this, { key: 'WardrobeScene', active: false });
                },
            preload: preloadWardrobeScene,
            create: createWardrobeScene,
            update: updateWardrobeScene

        });

        var SportsbagScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function SportsbagScene() {
                    Phaser.Scene.call(this, { key: 'SportsbagScene', active: false });
                },
            preload: preloadSportsbagScene,
            create: createSportsbagScene,
            update: updateSportsbagScene

        });

        var TreadmillScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function TreadmillScene() {
                    Phaser.Scene.call(this, { key: 'TreadmillScene', active: false });
                },
            preload: preloadTreadmillScene,
            create: createTreadmillScene,
            update: updateTreadmillScene

        });

        var BedScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function BedScene() {
                    Phaser.Scene.call(this, { key: 'BedScene', active: false });
                },
            preload: preloadBedScene,
            create: createBedScene,
            update: updateBedScene

        });

        var MapScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function MapScene() {
                    Phaser.Scene.call(this, { key: 'MapScene', active: false });
                },
            //preload: preloadBedScene,
            create: createMapScene,
            update: updateMapScene

        });

        var BoardScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function BoardScene() {
                    Phaser.Scene.call(this, { key: 'BoardScene', active: false });
                },
            //preload: preloadBedScene,
            create: createBoardScene,
            update: updateBoardScene

        });

        var ShelfScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function ShelfScene() {
                    Phaser.Scene.call(this, { key: 'ShelfScene', active: false });
                },
            //preload: preloadBedScene,
            create: createShelfScene,
            update: updateShelfScene

        });

        var LaptopScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function LaptopScene() {
                    Phaser.Scene.call(this, { key: 'LaptopScene', active: false });
                },
            //preload: preloadLaptopScene,
            create: createLaptopScene,
            update: updateLaptopScene

        });

        var Laptop2Scene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function Laptop2Scene() {
                    Phaser.Scene.call(this, { key: 'Laptop2Scene', active: false });
                },
            //preload: preloadLaptopScene,
            create: createLaptop2Scene,
            update: updateLaptop2Scene

        });

        var Laptop3Scene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function Laptop3Scene() {
                    Phaser.Scene.call(this, { key: 'Laptop3Scene', active: false });
                },
            //preload: preloadLaptopScene,
            create: createLaptop3Scene,
            update: updateLaptop3Scene

        });

        var DeskScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function DeskScene() {
                    Phaser.Scene.call(this, { key: 'DeskScene', active: false });
                },
            //preload: preloadBedScene,
            create: createDeskScene,
            update: updateDeskScene

        });

        var MagazineScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function DeskScene() {
                    Phaser.Scene.call(this, { key: 'MagazineScene', active: false });
                },
            //preload: preloadBedScene,
            create: createMagazineScene,
            update: updateMagazineScene

        });

        var MarathonScene = new Phaser.Class({

            Extends: Phaser.Scene,

            initialize:

                function MarathonScene() {
                    Phaser.Scene.call(this, { key: 'MarathonScene', active: false });
                },
            //preload: preloadBedScene,
            create: createMarathonScene,
            update: updateMarathonScene,

        });

        var config = {
            type: Phaser.AUTO,
            backgroundColor: '#FBFCFC',
            scale: {
                mode: Phaser.Scale.FIT,
                parent: 'phaser-example',
                pixelArt: true,
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
            dom: {
                createContainer: true
            },
            scene: [Preloader, FinalScene, MagazineScene, LaptopScene, Laptop2Scene, Laptop3Scene, DeskScene, ShelfScene, BoardScene, MapScene, BedScene, TreadmillScene, SportsbagScene, WardrobeScene, MainSceneR, MainScene0, StartScene, MarathonScene],
            audio: { disableWebAudio: true },
            physics: {
                default: "arcade"
            }
        };

        var velocity = -100;
        var velocityRunners = [];
        var marathonRestarted = false;
        var newBx, newBy;
        var bNum = 0;
        var buildingsWidth = [225, 450, 675, 675, 900, 1125, 1125, 1350];
        //var buildingsWidth = [150, 300, 450, 450, 600, 750, 750, 900];
        var hintLink = 'http://bit.ly/loesungmarathon';
        var youtubeLink = 'https://www.youtube.com/watch?v=MaIza_f69EE';
        var instaLink = 'https://instagram.com/runnerarmstretching';
        var depth = 100;
        var tap = 0;
        var printerCount;
        var fileL1;
        var fileL2;
        var fileL3;
        var printerPass = 0;
        var fileL1Pass = 0;
        var fileL2Pass = 0;
        var fileL3Pass = 0;
        var setA2 = false;
        var setB4 = false;
        var setC1 = false;
        var setD2 = false;
        var g_month = 0;
        var g_day = 29;
        var alphabet = ['A', 'B', 'C', 'D', 'E', 'F', 'J', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
        var countries = [0, 0, 0, 0, 0, 0, 0];
        var FlagsScene8XY_win = [[475, 330], [828, 250], [988, 335], [560, 880]];
        var FlagsScene8XY = [[300, 200], [350, 225], [335, 180], [330, 215]];
        var list1XY = [1175, 570];
        var list2XY = [1125, 580];
        var list3XY = [1150, 565];
        var list4XY = [1150, 550];
        var flag1Set = false;
        var flag2Set = false;
        var flag3Set = false;
        var flag4Set = false;
        var pageMag = 0;
        var g_spriteFlag1, g_spriteFlag2, g_spriteFlag3, g_spriteFlag4;
        var flag1Geom, flag2Geom, flag3Geom, flag4Geom;
        var mapZone1Geom, mapZone2Geom, mapZone3Geom, mapZone4Geom;
        var zoneA2, zoneB4, zoneC1, zoneD2;
        var ambient;
        var cick;
        var ambientOn = false;

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

        var listP1Ok = false;
        var listP2Ok = false;
        var listP3Ok = false;

        var book1Ok = false;
        var book2Ok = false;
        var book3Ok = false;

        var paperOk = false;
        var listOk = false;

        var laptopOn = false;
        var recordsOn = false;

        var winPrinter = false;

        var winBooks = false;
        var winBag = false;
        var winMap = false;
        var winTreadmill = false;
        var winFile = false;
        var winOpponents = false;

        var winShelf = false;

        var game = new Phaser.Game(config);


        function preloadMainScene0() {

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


        function createFinalScene() {

            imgStartScene = this.add.image(0, 0, 'imgFinal').setOrigin(0);
            this.sound.play('mp3Final');
        }

        function createStartScene() {

            imgStartScene = this.add.image(0, 0, 'imgStartBG').setOrigin(0);

            this.input.on('pointerdown', function (pointer, gameObject) {
                //this.scene.switch('MainScene0');

                this.cameras.main.fadeOut(1000);
                timedEvent = this.time.addEvent({ delay: 1250, callback: () => { this.scene.start('MainScene0'); }, callbackScope: this, repeat: 0, startAt: 0 });
                //timedEvent = this.time.addEvent({ delay: 1250, callback: () => { this.scene.start('MarathonScene'); }, callbackScope: this, repeat: 0, startAt: 0 });

            }, this);

        }

        function createMainScene0() {

            this.add.image(0, 0, 'imgWakeUp').setOrigin(0).setScale(1);
            var imgBag = this.add.image(940, 773, 'imgBagOpenMain0').setOrigin(0);
            if (sportsbagOpen) {
                imgBag.visible = true;
            } else {
                imgBag.visible = false;
            }
            this.cameras.main.fadeIn(6000);

            var fxCock = this.sound.add('mp3cock');
            fxCock.play();

            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_board = this.add.sprite(0, 0);
            var sprite_mainRight = this.add.sprite(0, 0);
            var sprite_wardrobe = this.add.sprite(0, 0);
            var sprite_soundBox = this.add.sprite(0, 0);
            var sprite_headBand = this.add.sprite(1255, 603, 'imgHeadbandMain0').setOrigin().setScale(1);
            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
            if (headbandPacked) {
                sprite_headBand.visible = false;
                sprite_headBand.disableInteractive();
            } else {
                sprite_headBand.visible = true;
                sprite_headBand.setInteractive();
            }

            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 540, 0, 540, 850, 0, 850]);
            var plgn_board = new Phaser.Geom.Polygon([0, 0, 540, 0, 540, 600, 400, 600, 400, 500, 200, 490, 200, 630, 0, 630]);
            var plgn_mainRight = new Phaser.Geom.Polygon([1100, 0, 1920, 0, 1920, 850, 1100, 850]);
            var plgn_wardrobe = new Phaser.Geom.Polygon([550, 0, 1050, 0, 1050, 900, 550, 900]);
            var plgn_soundBox = new Phaser.Geom.Polygon([1550, 700, 1920, 700, 1920, 900, 1550, 900]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_board.points, true);
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
            sprite_board.setInteractive(plgn_board, Phaser.Geom.Polygon.Contains);
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

                this.scene.start('DeskScene');

            }, this);

            sprite_board.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('BoardScene');

            }, this);

            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {

                this.scene.start('MainSceneR');

            }, this);

            sprite_wardrobe.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('WardrobeScene');

            }, this);

            sprite_soundBox.on('pointerdown', function (pointer, gameObject) {
                playAmbient();
            }, this);

            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });
        }

        function createMainSceneR() {

            this.add.image(0, 0, 'imgMainSceneRight').setOrigin(0);
            this.add.image(385, 0, 'imgWardrobeSceneMain2').setOrigin(0).setScale(1);
            var imgBag = this.add.image(575, 685, 'imgBagOpenMain2').setOrigin(0).setScale(1);
            if (sportsbagOpen) {
                imgBag.visible = true;
            } else {
                imgBag.visible = false;
            }
            if (g_spriteFlag1) {
                flag1X = g_spriteFlag1.x;
                flag1Y = g_spriteFlag1.y;

                flag2X = g_spriteFlag2.x;
                flag2Y = g_spriteFlag2.y;

                flag3X = g_spriteFlag3.x;
                flag3Y = g_spriteFlag3.y;

                flag4X = g_spriteFlag4.x;
                flag4Y = g_spriteFlag4.y;

            } else {
                flag1X = FlagsScene8XY[0][0];
                flag1Y = FlagsScene8XY[0][1];
                flag2X = FlagsScene8XY[1][0];
                flag2Y = FlagsScene8XY[1][1];
                flag3X = FlagsScene8XY[2][0];
                flag3Y = FlagsScene8XY[2][1];
                flag4X = FlagsScene8XY[3][0];
                flag4Y = FlagsScene8XY[3][1];
            }
            this.add.image((flag1X - 200) * 4 / 12 + 1200, (flag1Y - 100) * 3 / 9 + 200, 'imgFlag2').setOrigin(0).setScale(0.25);
            this.add.image((flag2X - 200) * 4 / 12 + 1200, (flag2Y - 100) * 3 / 9 + 200, 'imgFlag2').setOrigin(0).setScale(0.25);
            this.add.image((flag3X - 200) * 4 / 12 + 1200, (flag3Y - 100) * 3 / 9 + 200, 'imgFlag2').setOrigin(0).setScale(0.25);
            this.add.image((flag4X - 200) * 4 / 12 + 1200, (flag4Y - 100) * 3 / 9 + 200, 'imgFlag2').setOrigin(0).setScale(0.25);

            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
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
            var sprite_book1 = this.add.sprite(0, 0, 'book1.0').setOrigin(0);
            var sprite_book2 = this.add.sprite(0, 0, 'book1.1').setOrigin(0);
            var sprite_book3 = this.add.sprite(0, 0, 'book1.2').setOrigin(0);
            sprite_book1.visible = false;
            sprite_book2.visible = false;
            sprite_book3.visible = false;

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
            var plgn_wardrobe = new Phaser.Geom.Polygon([0, 0, 560, 0, 560, 1080, 0, 1080]);
            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 500, 330, 500, 330, 1080, 0, 1080]);
            var plgn_sportsBag = new Phaser.Geom.Polygon([440, 670, 720, 670, 720, 840, 570, 920, 440, 920]);
            var plgn_soundBox = new Phaser.Geom.Polygon([1240, 570, 1420, 590, 1420, 700, 1240, 680]);
            var plgn_books = new Phaser.Geom.Polygon([1200, 720, 1400, 720, 1400, 820, 1200, 820]);
            var plgn_bed = new Phaser.Geom.Polygon([1350, 860, 1630, 530, 1920, 530, 1920, 1080, 1350, 1080]);
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
            if (winBooks) {
                sprite_books.disableInteractive();
            }
            // if (!headBandPacked) {
            //     var sprite_headBand = this.add.sprite(1460, 910, 'imgPinUnconnected').setOrigin().setScale(1).setInteractive();
            //     this.input.setDraggable(sprite_headBand);
            // }

            sprite_treadmill.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('TreadmillScene');
            }, this);

            sprite_wardrobe.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('WardrobeScene');
            }, this);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {

                this.scene.start('DeskScene');

            }, this);

            sprite_sportsBag.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('SportsbagScene');
            }, this);

            sprite_soundBox.on('pointerdown', function (pointer, gameObject) {
                playAmbient();
            }, this);

            sprite_books.on('pointerdown', function (pointer, gameObject) {
                sprite_book1.visible = true;
                sprite_book1.setInteractive();
            }, this);

            sprite_book1.on('pointerdown', function (pointer, gameObject) {
                sprite_book1.visible = false;
                sprite_book1.disableInteractive();

                sprite_book2.visible = true;
                sprite_book2.setInteractive();

                fxPage = this.sound.add('mp3page');
                fxPage.play();
            }, this);

            sprite_book2.on('pointerdown', function (pointer, gameObject) {
                sprite_book2.visible = false;
                sprite_book2.disableInteractive();

                sprite_book3.visible = true;
                sprite_book3.setInteractive();

                fxPage = this.sound.add('mp3page');
                fxPage.play();
            }, this);

            sprite_book3.on('pointerdown', function (pointer, gameObject) {
                sprite_book3.visible = false;
                sprite_book3.disableInteractive();

                fxPage = this.sound.add('mp3page');
                fxPage.play();

                book1Ok = true;

                if (book1Ok && book2Ok && book3Ok) {
                    winBooks = true;
                    fxPage = this.sound.add('mp3Mark1');
                    fxPage.play();
                    this.scene.start('BoardScene');
                }
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

            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });

        }

        function createWardrobeScene() {

            this.add.image(0, 0, 'imgWardrobe').setOrigin(0);
            this.add.image(355, 355, 'imgBNGScene5').setOrigin(0).setScale(0.4);
            this.add.image(150, 380, 'imgBoardScene5').setOrigin(0);
            this.add.image(235, 595, 'imgBallScene5').setOrigin(0);
            this.add.image(255, 585, 'imgBallScene5').setOrigin(0);
            this.add.image(245, 575, 'imgBallScene5').setOrigin(0);
            var list = this.add.image(445, 590, 'imgListScene5').setOrigin(0).setScale(1.45);
            var listF = this.add.image(365, 545, 'imgListFScene5').setOrigin(0).setScale(0.11);
            if (listOk) {
                listF.visible = true;
                list.visible = false;
            } else {
                list.visible = true;
                listF.visible = false;
            }
            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_board = this.add.sprite(0, 0);
            var sprite_mainRight = this.add.sprite(0, 0);
            var sprite_wardrobe = this.add.sprite(0, 0);
            var sprite_books = this.add.sprite(0, 0);
            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
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
            var sprite_book1 = this.add.sprite(0, 0, 'book2.0').setOrigin(0);
            var sprite_book2 = this.add.sprite(0, 0, 'book2.1').setOrigin(0);
            sprite_book1.visible = false;
            sprite_book2.visible = false;

            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 550, 0, 550, 1080, 0, 1080]);
            var plgn_board = new Phaser.Geom.Polygon([0, 0, 550, 0, 550, 700, 0, 700]);
            var plgn_mainRight = new Phaser.Geom.Polygon([1350, 0, 1920, 0, 1920, 1080, 1350, 1080]);
            var plgn_wardrobe = new Phaser.Geom.Polygon([550, 0, 1350, 0, 1350, 1080, 550, 1080]);
            var plgn_books = new Phaser.Geom.Polygon([200, 0, 600, 0, 600, 400, 200, 400]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_board.points, true);
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
            sprite_board.setInteractive(plgn_board, Phaser.Geom.Polygon.Contains);
            sprite_mainRight.setInteractive(plgn_mainRight, Phaser.Geom.Polygon.Contains);
            sprite_wardrobe.setInteractive(plgn_wardrobe, Phaser.Geom.Polygon.Contains);
            sprite_books.setInteractive(plgn_books, Phaser.Geom.Polygon.Contains);
            if (winBooks) {
                sprite_books.disableInteractive();
            }
            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                if (wardrobeOpen) {
                    fxWardrobe = this.sound.add('mp3wClose');
                    fxWardrobe.play();
                    wardrobeOpen = false;
                }
                this.scene.start('DeskScene');

            }, this);

            sprite_board.on('pointerdown', function (pointer, gameObject) {
                if (wardrobeOpen) {
                    fxWardrobe = this.sound.add('mp3wClose');
                    fxWardrobe.play();
                    wardrobeOpen = false;
                }
                this.scene.start('BoardScene');

            }, this);

            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {
                if (wardrobeOpen) {
                    fxWardrobe = this.sound.add('mp3wClose');
                    fxWardrobe.play();
                    wardrobeOpen = false;
                }
                this.scene.start('MainSceneR');

            }, this);

            sprite_books.on('pointerdown', function (pointer, gameObject) {
                sprite_book1.visible = true;
                sprite_book1.setInteractive();
            }, this);

            sprite_book1.on('pointerdown', function (pointer, gameObject) {
                sprite_book1.visible = false;
                sprite_book1.disableInteractive();

                sprite_book2.visible = true;
                sprite_book2.setInteractive();

                fxPage = this.sound.add('mp3page');
                fxPage.play();
            }, this);

            sprite_book2.on('pointerdown', function (pointer, gameObject) {
                sprite_book2.visible = false;
                sprite_book2.disableInteractive();

                fxPage = this.sound.add('mp3page');
                fxPage.play();

                book2Ok = true;

                if (book1Ok && book2Ok && book3Ok) {
                    winBooks = true;
                    fxPage = this.sound.add('mp3Mark1');
                    fxPage.play();
                    this.scene.start('BoardScene');
                }
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
                    if (winBag) {
                        sprite_hat.disableInteractive();
                        sprite_shoesW.disableInteractive();
                        sprite_poloG.disableInteractive();
                        sprite_poloB.disableInteractive();
                        sprite_poloR.disableInteractive();
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
                    if (winBag) {
                        sprite_hat.disableInteractive();
                        sprite_shoesW.disableInteractive();
                        sprite_poloG.disableInteractive();
                        sprite_poloB.disableInteractive();
                        sprite_poloR.disableInteractive();
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

            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });
        }

        function createSportsbagScene() {

            imgScene = this.add.image(0, 0, 'imgSportsbag').setOrigin(0);



            var sprite_mainRight = this.add.sprite(0, 0);
            var sprite_sportsbag = this.add.sprite(0, 0);
            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
            var sprite_shoesR = this.add.sprite(1050, 320, 'imgShoesRScene6').setOrigin().setScale(1).setInteractive();
            var sprite_shoesW = this.add.sprite(1045, 300, 'imgShoesWScene6').setOrigin().setScale(1).setInteractive();
            var sprite_poloB = this.add.sprite(880, 480, 'imgPoloBScene6').setOrigin().setScale(1).setInteractive();
            var sprite_poloR = this.add.sprite(880, 480, 'imgPoloRScene6').setOrigin().setScale(1).setInteractive();
            var sprite_poloG = this.add.sprite(880, 480, 'imgPoloGScene6').setOrigin().setScale(1).setInteractive();
            var sprite_shirt = this.add.sprite(880, 460, 'imgShirtScene6').setOrigin().setScale(1).setInteractive();
            var sprite_pants = this.add.sprite(1125, 532, 'imgPantsScene6').setOrigin().setScale(1).setInteractive();
            var sprite_tracker = this.add.sprite(900, 500, 'imgTracker').setOrigin().setScale(1.2).setInteractive();
            var sprite_clock = this.add.sprite(1000, 450, 'imgClock').setOrigin().setScale(1.1).setInteractive();
            var sprite_armband = this.add.sprite(950, 540, 'imgArmbandScene6').setOrigin().setScale(1).setInteractive();
            var sprite_hat = this.add.sprite(810, 565, 'imgHatScene6').setOrigin().setScale(1).setInteractive();
            var sprite_headband = this.add.sprite(790, 390, 'imgHeadbandScene6').setOrigin().setScale(0.9).setInteractive();

            if (hatPacked) {
                sprite_hat.visible = true;
                sprite_hat.setInteractive();
            } else {
                sprite_hat.visible = false;
                sprite_hat.disableInteractive();
            }
            if (headbandPacked) {
                sprite_headband.visible = true;
                sprite_headband.setInteractive();
            } else {
                sprite_headband.visible = false;
                sprite_headband.disableInteractive();
            }
            if (shoesRPacked) {
                sprite_shoesR.visible = true;
                sprite_shoesR.setInteractive();
            } else {
                sprite_shoesR.visible = false;
                sprite_shoesR.disableInteractive();
            }
            if (shoesWPacked) {
                sprite_shoesW.visible = true;
                sprite_shoesW.setInteractive();
            } else {
                sprite_shoesW.visible = false;
                sprite_shoesW.disableInteractive();
            }
            if (poloGPacked) {
                sprite_poloG.visible = true;
                sprite_poloG.setInteractive();
            } else {
                sprite_poloG.visible = false;
                sprite_poloG.disableInteractive();
            }
            if (poloBPacked) {
                sprite_poloB.visible = true;
                sprite_poloB.setInteractive();
            } else {
                sprite_poloB.visible = false;
                sprite_poloB.disableInteractive();
            }
            if (poloRPacked) {
                sprite_poloR.visible = true;
                sprite_poloR.setInteractive();
            } else {
                sprite_poloR.visible = false;
                sprite_poloR.disableInteractive();
            }
            if (shirtPacked) {
                sprite_shirt.visible = true;
                sprite_shirt.setInteractive();
            } else {
                sprite_shirt.visible = false;
                sprite_shirt.disableInteractive();
            }
            if (pantsPacked) {
                sprite_pants.visible = true;
                sprite_pants.setInteractive();
            } else {
                sprite_pants.visible = false;
                sprite_pants.disableInteractive();
            }
            if (clockPacked) {
                sprite_clock.visible = true;
                sprite_clock.setInteractive();
            } else {
                sprite_clock.visible = false;
                sprite_clock.disableInteractive();
            }
            if (armbandPacked) {
                sprite_armband.visible = true;
                sprite_armband.setInteractive();
            } else {
                sprite_armband.visible = false;
                sprite_armband.disableInteractive();
            }
            if (trackerPacked) {
                sprite_tracker.visible = true;
                sprite_tracker.setInteractive();
            } else {
                sprite_tracker.visible = false;
                sprite_tracker.disableInteractive();
            }

            var sprite_bagOpen = this.add.sprite(580, 18, 'imgBagOpen').setOrigin(0).setScale(1).setInteractive();
            var sprite_bagClose = this.add.sprite(607, 21, 'imgBagClose').setOrigin(0).setScale(1).setInteractive();
            imgScene = this.add.image(0, 0, 'imgSportsbagL').setOrigin(0);
            if (sportsbagOpen) {
                sprite_bagOpen.visible = true;
                sprite_bagOpen.setInteractive();
                sprite_bagClose.visible = false;
                sprite_bagClose.disableInteractive();
            } else {
                sprite_bagOpen.visible = false;
                sprite_bagOpen.disableInteractive();
                sprite_bagClose.visible = true;
                sprite_bagClose.setInteractive();
            }
            var sprite_listP3 = this.add.sprite(625, 290, 'imgListPart3').setOrigin(0).setAngle(-120).setScale(1.75).setInteractive();
            if (listP3Ok) sprite_listP3.visible = false;

            var plgn_mainRight = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_sportsbag = new Phaser.Geom.Polygon([500, 520, 990, 0, 1500, 0, 1580, 420, 1000, 1080, 800, 1080, 500, 730]);

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


            sprite_listP3.on('pointerdown', function (pointer, gameObject) {
                this.sound.play('mp3Sheet');
                listP3Ok = true;
                sprite_listP3.visible = false;
            }, this);


            sprite_sportsbag.on('pointerdown', function (pointer, gameObject) {
                if (!winBag) {
                    var fxZip;
                    if (sportsbagOpen) {
                        fxZip = this.sound.add('mp3zip');
                        sprite_bagOpen.visible = false;
                        sprite_bagOpen.disableInteractive();
                        sprite_bagClose.visible = true;
                        sprite_bagClose.setInteractive();
                    } else {
                        fxZip = this.sound.add('mp3unzip');
                        sprite_bagOpen.visible = true;
                        sprite_bagOpen.setInteractive();
                        sprite_bagClose.visible = false;
                        sprite_bagClose.disableInteractive();
                    }

                    fxZip.play();
                    sportsbagOpen = !sportsbagOpen;

                    if (headbandPacked && shoesRPacked && shirtPacked && armbandPacked && pantsPacked) {
                        winBag = true;
                        fxPage = this.sound.add('mp3Mark1');


                        timedEvent = this.time.addEvent({
                            delay: 750, callback: () => {
                                this.scene.start('BoardScene');
                                fxPage.play();
                            }, callbackScope: this, repeat: 0, startAt: 0
                        });
                    }
                }


            }, this);

            sprite_bagOpen.on('pointerdown', function (pointer, gameObject) {

                if (!winBag) {
                    fxZip = this.sound.add('mp3zip');
                    sprite_bagOpen.visible = false;
                    sprite_bagOpen.disableInteractive();
                    sprite_bagClose.visible = true;
                    sprite_bagClose.setInteractive();

                    fxZip.play();
                    sportsbagOpen = !sportsbagOpen;

                    if (headbandPacked && shoesRPacked && shirtPacked && armbandPacked && pantsPacked) {
                        winBag = true;
                        fxPage = this.sound.add('mp3Mark1');
                        timedEvent = this.time.addEvent({
                            delay: 750, callback: () => {
                                this.scene.start('BoardScene');
                                fxPage.play();
                            }, callbackScope: this, repeat: 0, startAt: 0
                        });
                    }
                }



            }, this);

            sprite_bagClose.on('pointerdown', function (pointer, gameObject) {

                if (!winBag) {
                    fxZip = this.sound.add('mp3unzip');
                    sprite_bagOpen.visible = true;
                    sprite_bagOpen.setInteractive();
                    sprite_bagClose.visible = false;
                    sprite_bagClose.disableInteractive();


                    fxZip.play();
                    sportsbagOpen = !sportsbagOpen;


                }



            }, this);

            sprite_hat.on('pointerdown', function (pointer, gameObject) {

                hatPacked = false;
                sprite_hat.visible = false;
                sprite_hat.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_headband.on('pointerdown', function (pointer, gameObject) {

                headbandPacked = false;
                sprite_headband.visible = false;
                sprite_headband.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_shoesR.on('pointerdown', function (pointer, gameObject) {

                shoesRPacked = false;
                sprite_shoesR.visible = false;
                sprite_shoesR.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_shoesW.on('pointerdown', function (pointer, gameObject) {

                shoesWPacked = false;
                sprite_shoesW.visible = false;
                sprite_shoesW.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_poloB.on('pointerdown', function (pointer, gameObject) {

                poloBPacked = false;
                sprite_poloB.visible = false;
                sprite_poloB.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_poloG.on('pointerdown', function (pointer, gameObject) {

                poloGPacked = false;
                sprite_poloG.visible = false;
                sprite_poloG.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_poloR.on('pointerdown', function (pointer, gameObject) {

                poloRPacked = false;
                sprite_poloR.visible = false;
                sprite_poloR.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_shirt.on('pointerdown', function (pointer, gameObject) {

                shirtPacked = false;
                sprite_shirt.visible = false;
                sprite_shirt.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_pants.on('pointerdown', function (pointer, gameObject) {

                pantsPacked = false;
                sprite_pants.visible = false;
                sprite_pants.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_clock.on('pointerdown', function (pointer, gameObject) {

                clockPacked = false;
                sprite_clock.visible = false;
                sprite_clock.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_tracker.on('pointerdown', function (pointer, gameObject) {

                trackerPacked = false;
                sprite_tracker.visible = false;
                sprite_tracker.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_armband.on('pointerdown', function (pointer, gameObject) {

                armbandPacked = false;
                sprite_armband.visible = false;
                sprite_armband.disableInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });
        }

        function createTreadmillScene() {

            imgScene = this.add.image(0, 0, 'imgTreadmill').setOrigin(0);
            var imgReady = this.add.image(1050, 100, 'imgReady').setOrigin(0).setScale(0.2);
            var imgSteady = this.add.image(1050, 100, 'imgSteady').setOrigin(0).setScale(0.2);
            var imgGo = this.add.image(1050, 100, 'imgGo').setOrigin(0).setScale(0.2);
            var imgFaster = this.add.image(1050, 100, 'imgFaster').setOrigin(0).setScale(0.2);
            var imgGood = this.add.image(1050, 100, 'imgGood').setOrigin(0).setScale(0.2);
            var imgFail = this.add.image(1050, 100, 'imgFail').setOrigin(0).setScale(0.2);
            var imgPB = this.add.image(900, 660, 'imgPB').setOrigin(0).setScale(0.1);

            imgReady.visible = false;
            imgSteady.visible = false;
            imgGo.visible = false;
            imgFaster.visible = false;
            imgGood.visible = false;
            imgFail.visible = false;
            imgPB.visible = false;


            if (g_spriteFlag1) {
                flag1X = g_spriteFlag1.x;
                flag1Y = g_spriteFlag1.y;

                flag2X = g_spriteFlag2.x;
                flag2Y = g_spriteFlag2.y;

                flag3X = g_spriteFlag3.x;
                flag3Y = g_spriteFlag3.y;

                flag4X = g_spriteFlag4.x;
                flag4Y = g_spriteFlag4.y;

            } else {
                flag1X = FlagsScene8XY[0][0];
                flag1Y = FlagsScene8XY[0][1];
                flag2X = FlagsScene8XY[1][0];
                flag2Y = FlagsScene8XY[1][1];
                flag3X = FlagsScene8XY[2][0];
                flag3Y = FlagsScene8XY[2][1];
                flag4X = FlagsScene8XY[3][0];
                flag4Y = FlagsScene8XY[3][1];
            }
            this.add.image((flag1X - 200) * 8 / 14 + 1400, (flag1Y - 100) * 43 / 66 + 105, 'imgFlag2').setOrigin(0).setScale(0.6);
            this.add.image((flag2X - 200) * 8 / 14 + 1400, (flag2Y - 100) * 43 / 66 + 105, 'imgFlag2').setOrigin(0).setScale(0.6);
            this.add.image((flag3X - 200) * 8 / 14 + 1400, (flag3Y - 100) * 43 / 66 + 105, 'imgFlag2').setOrigin(0).setScale(0.6);
            this.add.image((flag4X - 200) * 8 / 14 + 1400, (flag4Y - 100) * 43 / 66 + 105, 'imgFlag2').setOrigin(0).setScale(0.6);


            var fxTreadmill = this.sound.add('mp3treadmill', { loop: 1, volume: 0.06 });
            var bgTreadmill = this.sound.add('mp3run');

            var fxStepL = this.sound.add('mp3stepL', { volume: 0.25 });
            var fxStepR = this.sound.add('mp3stepR', { volume: 0.25 });
            var stepL = true;

            var sprite_mainRight = this.add.sprite(0, 0);
            var sprite_treadmill = this.add.sprite(0, 0);
            var sprite_treadmillStart = this.add.sprite(0, 0);
            var sprite_map = this.add.sprite(0, 0);
            var sprite_soundBox = this.add.sprite(0, 0);
            var step = this.add.sprite(848, 955, 'imgStep').setOrigin().setScale(0.225);
            step.visible = false;

            var sprite_headBand = this.add.sprite(1115, 940, 'imgHeadbandScene7').setOrigin().setScale(1);
            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
            if (headbandPacked) {
                sprite_headBand.visible = false;
                sprite_headBand.disableInteractive();
            } else {
                sprite_headBand.visible = true;
                sprite_headBand.setInteractive();
            }

            var groupD1 = this.add.group();
            for (var i = 0; i <= 9; i++) {
                groupD1.create(745, 660, 'imgTreadmillD' + i).setOrigin(0).setScale(0.2);
            }
            var childD1 = groupD1.getChildren();
            for (var i = 0; i < 10; i++) {
                childD1[i].visible = false;
            }

            var groupD2 = this.add.group();
            for (var i = 0; i <= 9; i++) {
                groupD2.create(785, 660, 'imgTreadmillD' + i).setOrigin(0).setScale(0.2);
            }
            var childD2 = groupD2.getChildren();
            for (var i = 0; i < 10; i++) {
                childD2[i].visible = false;
            }

            var groupD3 = this.add.group();
            for (var i = 0; i <= 9; i++) {
                groupD3.create(825, 660, 'imgTreadmillD' + i).setOrigin(0).setScale(0.2);
            }
            var childD3 = groupD3.getChildren();
            for (var i = 0; i < 10; i++) {
                childD3[i].visible = false;
            }

            if (winTreadmill) {
                childD1[(tap % 1000 - tap % 100) / 100].visible = true;
                childD2[(tap % 100 - tap % 10) / 10].visible = true;
                childD3[tap % 10].visible = true;
                imgPB.visible = true;
            }

            var plgn_mainRight = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_treadmillStart = new Phaser.Geom.Polygon([630, 620, 1020, 620, 1020, 810, 630, 810]);
            var plgn_treadmill = new Phaser.Geom.Polygon([450, 0, 1280, 0, 1280, 1080, 450, 1080]);
            var plgn_map = new Phaser.Geom.Polygon([1480, 115, 1920, 100, 1920, 670, 1480, 650]);
            var plgn_soundBox = new Phaser.Geom.Polygon([1530, 870, 1920, 870, 1920, 1080, 1530, 1080]);

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
            sprite_soundBox.setInteractive(plgn_soundBox, Phaser.Geom.Polygon.Contains);
            sprite_map.setInteractive(plgn_map, Phaser.Geom.Polygon.Contains);


            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {

                this.scene.start('MainSceneR');

            }, this);

            step.on('pointerdown', function (pointer, gameObject) {
                tap += 15;
                for (var i = 0; i < 10; i++) {
                    childD1[i].visible = false;
                    childD2[i].visible = false;
                    childD3[i].visible = false;
                }
                childD1[(tap % 1000 - tap % 100) / 100].visible = true;
                childD2[(tap % 100 - tap % 10) / 10].visible = true;
                childD3[tap % 10].visible = true;
                fxTreadmill.play();

                //step.visible = false;
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
                fxBttn = this.sound.add('mp3Bttn');
                fxBttn.play();
                imgFail.visible = false;
                if (!winTreadmill) {
                    if (!treadmillRun) {
                        treadmillRun = true;
                        if (ambient.isPlaying) {
                            ambient.pause();
                        }
                        sprite_mainRight.disableInteractive();
                        sprite_map.disableInteractive();
                        sprite_soundBox.disableInteractive();
                        //sprite_mainRight.stopPropagation();

                        //timerTreadmill = this.sys.game.loop.time;

                        timedEvent = this.time.addEvent({
                            delay: 1000, callback: () => {
                                for (var i = 0; i < 10; i++) {
                                    childD1[i].visible = false;
                                    childD2[i].visible = false;
                                    childD3[i].visible = false;
                                }
                                childD1[0].visible = true;
                                childD2[0].visible = true;
                                childD3[0].visible = true;
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
                            delay: 4875.61, callback: () => {

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
                            delay: 5225.61, callback: () => {

                                imgSteady.visible = false;
                                imgGo.visible = true;
                                // step.visible = true;
                                // step.setInteractive();


                                timedEvent3 = this.time.addEvent({
                                    delay: 487.80, callback: () => {

                                        step.visible = false;
                                        step.disableInteractive();
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


                                if (tap < 365) {
                                    imgFaster.visible = true;
                                }
                                if (tap > 390) {
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
                                if (tap < 870) {
                                    fxBreath = this.sound.add('mp3breath');
                                    fxBreath.play();
                                    tap = 0;
                                    imgFail.visible = true;
                                } else {
                                    winTreadmill = true;
                                    fxBreath = this.sound.add('mp3fanfair');
                                    fxBreath.play();
                                    imgPB.visible = true;
                                    sprite_treadmillStart.disableInteractive();
                                }

                            }, callbackScope: this, repeat: 0, startAt: 0
                        });


                        timedEvent = this.time.addEvent({
                            delay: 34740, callback: () => {

                                // imgGo.visible = false;
                                treadmillRun = false;
                                fxTreadmill.stop();
                                bgTreadmill.stop();
                                step.visible = false;
                                step.disableInteractive();
                                sprite_mainRight.setInteractive(plgn_mainRight, Phaser.Geom.Polygon.Contains);
                                sprite_soundBox.setInteractive(plgn_soundBox, Phaser.Geom.Polygon.Contains);
                                sprite_map.setInteractive(plgn_map, Phaser.Geom.Polygon.Contains);

                                if (!winTreadmill) {
                                    childD1[0].visible = true;
                                    childD2[0].visible = true;
                                    childD3[0].visible = true;
                                }




                            }, callbackScope: this, repeat: 0, startAt: 0
                        });

                        timedEvent = this.time.addEvent({
                            delay: 37000, callback: () => {
                                if (winTreadmill) {
                                    fxPage = this.sound.add('mp3Mark1');

                                    this.scene.start('BoardScene');
                                    fxPage.play();
                                }
                            }, callbackScope: this, repeat: 0, startAt: 0
                        });

                    }

                }

            }, this);


            sprite_soundBox.on('pointerdown', function (pointer, gameObject) {
                playAmbient();
            }, this);

            sprite_map.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('MapScene');

            }, this);

            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });

        }

        function createBedScene() {

            imgScene = this.add.image(0, 0, 'imgBed').setOrigin(0);

            var sprite_mainRight = this.add.sprite(0, 0);
            var sprite_bed = this.add.sprite(0, 0);
            var sprite_soundBox = this.add.sprite(0, 0);
            var sprite_books = this.add.sprite(0, 0);
            var sprite_map = this.add.sprite(0, 0);
            var sprite_pants = this.add.sprite(1400, 740, 'imgPantsScene9').setOrigin(0).setInteractive();

            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;

            if (pantsPacked) {
                sprite_pants.visible = false;
                sprite_pants.disableInteractive();
            } else {
                sprite_pants.visible = true;
                sprite_pants.setInteractive();
            }

            var sprite_book1 = this.add.sprite(0, 0, 'book1.0').setOrigin(0);
            var sprite_book2 = this.add.sprite(0, 0, 'book1.1').setOrigin(0);
            var sprite_book3 = this.add.sprite(0, 0, 'book1.2').setOrigin(0);
            sprite_book1.visible = false;
            sprite_book2.visible = false;
            sprite_book3.visible = false;

            var plgn_mainRight = new Phaser.Geom.Polygon([0, 800, 720, 700, 1000, 1080, 0, 1080]);
            var plgn_bed = new Phaser.Geom.Polygon([700, 320, 1300, 320, 1300, 470, 700, 550]);
            var plgn_soundBox = new Phaser.Geom.Polygon([100, 300, 430, 330, 430, 530, 100, 480]);
            var plgn_books = new Phaser.Geom.Polygon([230, 620, 420, 590, 430, 720, 230, 750]);
            var plgn_map = new Phaser.Geom.Polygon([50, 0, 1000, 0, 1000, 150, 50, 150]);

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
            if (winBooks) {
                sprite_books.disableInteractive();
            }
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

                g_day++;
                if (g_month == 0 && g_day >= 32) { g_month = 1; g_day = 1; }
                if (g_month == 1 && g_day >= 29) { g_month = 2; g_day = 1; }
                if (g_month == 2 && g_day >= 32) { g_month = 3; g_day = 1; }
                if (g_month == 3 && g_day >= 31) { g_month = 4; g_day = 1; }
                if (g_month == 4 && g_day >= 32) { g_month = 5; g_day = 1; }
                if (g_month == 5 && g_day >= 31) { g_month = 6; g_day = 1; }
                if (g_month == 6 && g_day >= 32) { g_month = 7; g_day = 1; }
                if (g_month == 7 && g_day >= 32) { g_month = 8; g_day = 1; }
                if (g_month == 8 && g_day >= 31) { g_month = 9; g_day = 1; }
                if (g_month == 9 && g_day >= 32) { g_month = 10; g_day = 1; }
                if (g_month == 10 && g_day >= 31) { g_month = 11; g_day = 1; }
                if (g_month == 11 && g_day >= 32) { g_month = 0; g_day = 1; }



                this.sound.play('mp3yawn');
                this.cameras.main.fadeOut(3000);
                if (g_month == 2 && g_day == 25 && winBooks && winBag && winMap && winTreadmill && winFile && winOpponents) {

                    timedEvent = this.time.addEvent({
                        delay: 4000, callback: () => {
                            ambient.pause();
                            this.scene.start('MarathonScene');

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                } else {
                    timedEvent = this.time.addEvent({
                        delay: 3250, callback: () => {

                            this.scene.start('MainScene0');

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });
                }




            }, this);

            sprite_soundBox.on('pointerdown', function (pointer, gameObject) {

                playAmbient();

            }, this);

            sprite_books.on('pointerdown', function (pointer, gameObject) {
                sprite_book1.visible = true;
                sprite_book1.setInteractive();
            }, this);

            sprite_book1.on('pointerdown', function (pointer, gameObject) {
                sprite_book1.visible = false;
                sprite_book1.disableInteractive();

                sprite_book2.visible = true;
                sprite_book2.setInteractive();

                fxPage = this.sound.add('mp3page');
                fxPage.play();
            }, this);

            sprite_book2.on('pointerdown', function (pointer, gameObject) {
                sprite_book2.visible = false;
                sprite_book2.disableInteractive();

                sprite_book3.visible = true;
                sprite_book3.setInteractive();

                fxPage = this.sound.add('mp3page');
                fxPage.play();
            }, this);

            sprite_book3.on('pointerdown', function (pointer, gameObject) {
                sprite_book3.visible = false;
                sprite_book3.disableInteractive();

                fxPage = this.sound.add('mp3page');
                fxPage.play();

                book1Ok = true;

                if (book1Ok && book2Ok && book3Ok) {
                    winBooks = true;
                    fxPage = this.sound.add('mp3Mark1');
                    fxPage.play();
                    this.scene.start('BoardScene');
                }
            }, this);


            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_map.on('pointerdown', function (pointer, gameObject) {

                this.scene.switch('MapScene');

            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });

        }

        function createMapScene() {

            imgScene = this.add.image(0, 0, 'imgMap').setOrigin(0).setScale(1);
            var imgRoute = this.add.image(466, 265, 'imgTrack1').setOrigin(0).setScale(1);
            if (!winMap) {
                imgRoute.visible = false;
            }

            //this.add.image(725, 472, 'imgTrack3').setOrigin(0).setScale(1);

            var mapLeave = false;
            var sprite_mainRight = this.add.sprite(0, 0);
            var sprite_map = this.add.sprite(0, 0);
            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
            var sprite_zoneA2 = this.add.sprite(0, 0);
            var sprite_zoneB4 = this.add.sprite(0, 0);
            var sprite_zoneC1 = this.add.sprite(0, 0);
            var sprite_zoneD2 = this.add.sprite(0, 0);

            var zoneMap = this.add.zone(0, 0).setOrigin(0);
            var zoneA2 = this.add.zone(0, 0).setOrigin(0);
            var zoneB4 = this.add.zone(0, 0).setOrigin(0);
            var zoneC1 = this.add.zone(0, 0).setOrigin(0);
            var zoneD2 = this.add.zone(0, 0).setOrigin(0);

            zoneMap.setName('zMap');
            zoneA2.setName('zA2');
            zoneB4.setName('zB4');
            zoneC1.setName('zC1');
            zoneD2.setName('zD2');

            g_spriteFlag1 = this.add.sprite(0, 0, 'imgFlag').setOrigin(0).setScale(0.075 - (3 / 125000) * FlagsScene8XY[0][1]).setInteractive();
            g_spriteFlag2 = this.add.sprite(0, 0, 'imgFlag').setOrigin(0).setScale(0.075 - (3 / 125000) * FlagsScene8XY[1][1]).setInteractive();
            g_spriteFlag3 = this.add.sprite(0, 0, 'imgFlag').setOrigin(0).setScale(0.075 - (3 / 125000) * FlagsScene8XY[2][1]).setInteractive();
            g_spriteFlag4 = this.add.sprite(0, 0, 'imgFlag').setOrigin(0).setScale(0.075 - (3 / 125000) * FlagsScene8XY[3][1]).setInteractive();
            g_spriteFlag1.x = FlagsScene8XY[0][0];
            g_spriteFlag1.y = FlagsScene8XY[0][1];
            g_spriteFlag2.x = FlagsScene8XY[1][0];
            g_spriteFlag2.y = FlagsScene8XY[1][1];
            g_spriteFlag3.x = FlagsScene8XY[2][0];
            g_spriteFlag3.y = FlagsScene8XY[2][1];
            g_spriteFlag4.x = FlagsScene8XY[3][0];
            g_spriteFlag4.y = FlagsScene8XY[3][1];
            this.input.setDraggable(g_spriteFlag1);
            this.input.setDraggable(g_spriteFlag2);
            this.input.setDraggable(g_spriteFlag3);
            this.input.setDraggable(g_spriteFlag4);
            g_spriteFlag1.setName('f1');
            g_spriteFlag2.setName('f2');
            g_spriteFlag3.setName('f3');
            g_spriteFlag4.setName('f4');
            var plgn_mainRight = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_map = new Phaser.Geom.Polygon([270, 60, 1350, 180, 1350, 870, 270, 980]);

            var plgn_A2 = new Phaser.Geom.Polygon([260, 290, 560, 300, 560, 530, 260, 520]);
            var plgn_B4 = new Phaser.Geom.Polygon([490, 730, 755, 730, 755, 940, 495, 960]);
            var plgn_C1 = new Phaser.Geom.Polygon([690, 100, 935, 120, 935, 330, 690, 325]);
            var plgn_D2 = new Phaser.Geom.Polygon([885, 330, 1105, 330, 1105, 530, 880, 525]);

            sprite_zoneA2.setInteractive(plgn_A2, Phaser.Geom.Polygon.Contains);
            sprite_zoneB4.setInteractive(plgn_B4, Phaser.Geom.Polygon.Contains);
            sprite_zoneC1.setInteractive(plgn_C1, Phaser.Geom.Polygon.Contains);
            sprite_zoneD2.setInteractive(plgn_D2, Phaser.Geom.Polygon.Contains);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_A2.points, true);
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_B4.points, true);
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_C1.points, true);
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_D2.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainRight.setInteractive(plgn_mainRight, Phaser.Geom.Polygon.Contains);
            sprite_map.setInteractive(plgn_map, Phaser.Geom.Polygon.Contains);


            zoneMap.setInteractive(plgn_map, Phaser.Geom.Polygon.Contains);
            zoneA2.setInteractive(plgn_A2, Phaser.Geom.Polygon.Contains);
            zoneB4.setInteractive(plgn_B4, Phaser.Geom.Polygon.Contains);
            zoneC1.setInteractive(plgn_C1, Phaser.Geom.Polygon.Contains);
            zoneD2.setInteractive(plgn_D2, Phaser.Geom.Polygon.Contains);

            zoneMap.input.dropZone = true;
            zoneA2.input.dropZone = true;
            zoneB4.input.dropZone = true;
            zoneC1.input.dropZone = true;
            zoneD2.input.dropZone = true;


            var getFromA2 = false;
            var getFromB4 = false;
            var getFromC1 = false;
            var getFromD2 = false;


            sprite_mainRight.on('pointerdown', function (pointer, gameObject) {
                this.scene.start('MainSceneR');
            }, this);

            this.input.on('drag', function (pointer, gameObject, dragX, dragY) {

                if (dragX > 270 && dragX < 1350) {
                    gameObject.x = dragX;
                }

                if (dragY > 105 && dragY < 935) {
                    gameObject.y = dragY;
                }


                gameObject.setScale(0.075 - (3.63 / 190000) * gameObject.x);

                FlagsScene8XY[0][0] = g_spriteFlag1.x;
                FlagsScene8XY[0][1] = g_spriteFlag1.y;
                FlagsScene8XY[1][0] = g_spriteFlag2.x;
                FlagsScene8XY[1][1] = g_spriteFlag2.y;
                FlagsScene8XY[2][0] = g_spriteFlag3.x;
                FlagsScene8XY[2][1] = g_spriteFlag3.y;
                FlagsScene8XY[3][0] = g_spriteFlag4.x;
                FlagsScene8XY[3][1] = g_spriteFlag4.y;

            });


            this.input.on('dragenter', function (pointer, gameObject, dropZone) {
                if (dropZone.name == 'zMap') {
                    mapLeave = false;

                }
                if (dropZone.name == 'zA2') {

                    if (mapLeave) {
                        setA2++;

                    } else {
                        if (setA2) {
                            setA2--;
                            getFromA2 = true;
                        }
                    }

                }

                if (dropZone.name == 'zB4') {
                    if (mapLeave) {
                        setB4++;

                    } else {
                        if (setB4) {
                            setB4--;
                            getFromB4 = true;
                        }

                    }
                }

                if (dropZone.name == 'zC1') {
                    if (mapLeave) {
                        setC1++;

                    } else {
                        if (setC1) {
                            setC1--;
                            getFromC1 = true;
                        }
                    }
                }

                if (dropZone.name == 'zD2') {
                    if (mapLeave) {
                        setD2++;

                    } else {
                        if (setD2) {
                            setD2--;
                            getFromD2 = true;
                        }
                    }
                }

            });

            this.input.on('dragleave', function (pointer, gameObject, dropZone) {
                if (dropZone.name == 'zMap') {
                    mapLeave = true;
                }
                if (dropZone.name == 'zA2') {
                    if (setA2) setA2--;
                    if (getFromA2 && setA2) { setA2++; getFromA2 = false; }

                }

                if (dropZone.name == 'zB4') {
                    if (setB4) setB4--;
                    if (getFromB4 && setB4) { setB4++; getFromB4 = false; }
                }

                if (dropZone.name == 'zC1') {
                    if (setC1) setC1--;
                    if (getFromC1 && setC1) { setC1++; getFromC1 = false; }
                }

                if (dropZone.name == 'zD2') {
                    if (setD2) setD2--;
                    if (getFromD2 && setD2) { setD2++; getFromD2 = false; }
                }

            });

            this.input.on('drop', function (pointer, gameObject, dropZone) {
                game.sound.play('mp3Flag');

                if (dropZone.name == 'zA2') {

                    if (!mapLeave) {
                        setA2++;

                    }

                }

                if (dropZone.name == 'zB4') {
                    if (!mapLeave) {
                        setB4++;

                    }
                }

                if (dropZone.name == 'zC1') {
                    if (!mapLeave) {
                        setC1++;

                    }
                }

                if (dropZone.name == 'zD2') {
                    if (!mapLeave) {
                        setD2++;

                    }
                }
                mapLeave = false;


                if (setA2 && setB4 && setC1 && setD2) {
                    winMap = true;
                    imgRoute.visible = true;
                    g_spriteFlag1.x = FlagsScene8XY_win[0][0];
                    g_spriteFlag1.y = FlagsScene8XY_win[0][1];
                    g_spriteFlag2.x = FlagsScene8XY_win[1][0];
                    g_spriteFlag2.y = FlagsScene8XY_win[1][1];
                    g_spriteFlag3.x = FlagsScene8XY_win[2][0];
                    g_spriteFlag3.y = FlagsScene8XY_win[2][1];
                    g_spriteFlag4.x = FlagsScene8XY_win[3][0];
                    g_spriteFlag4.y = FlagsScene8XY_win[3][1];

                    g_spriteFlag1.disableInteractive();
                    g_spriteFlag2.disableInteractive();
                    g_spriteFlag3.disableInteractive();
                    g_spriteFlag4.disableInteractive();

                    fxPage = game.sound.add('mp3Mark1');
                    fxPage.play();

                }
            });


            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });

        }

        function createBoardScene() {

            this.add.image(0, 0, 'imgBoard').setOrigin(0);
            this.add.image(1050, 200, 'imgBNG').setOrigin(0).setScale(0.8).setAngle(-5);;
            this.add.image(350, 820, 'imgSticker').setOrigin(0);
            this.add.image(700, 210, 'imgBoardFlag2').setOrigin(0).setScale(0.12).setAngle(-12);
            shelfOpen = false;
            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_board = this.add.sprite(0, 0);
            var sprite_wardrobe = this.add.sprite(0, 0);
            var sprite_poster = this.add.sprite(450, 270, 'imgPoster').setOrigin(0).setScale(0.15);
            var sprite_checklistW = this.add.sprite(360, 160, 'imgChecklistW').setOrigin(0);
            var sprite_checklist = this.add.sprite(360, 160, 'imgChecklist').setOrigin(0).setInteractive();
            sprite_checklistW.setName('sChecklistW');
            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
            var img_check1 = this.add.image(415, 215, 'imgCheck').setOrigin(0);
            var img_check2 = this.add.image(417, 244, 'imgCheck').setOrigin(0);
            var img_check3 = this.add.image(420, 271, 'imgCheck').setOrigin(0);
            var img_check4 = this.add.image(422, 301, 'imgCheck').setOrigin(0);
            var img_check5 = this.add.image(424, 330, 'imgCheck').setOrigin(0);
            var img_check6 = this.add.image(427, 356, 'imgCheck').setOrigin(0);

            if (winBooks) {
                img_check1.visible = true;
            } else {
                img_check1.visible = false;
            }
            if (winBag) {
                img_check2.visible = true;
            } else {
                img_check2.visible = false;
            }
            if (winMap) {
                img_check3.visible = true;
            } else {
                img_check3.visible = false;
            }
            if (winTreadmill) {
                img_check4.visible = true;
            } else {
                img_check4.visible = false;
            }
            if (winFile) {
                img_check5.visible = true;
            } else {
                img_check5.visible = false;
            }
            if (winOpponents) {
                img_check6.visible = true;
            } else {
                img_check6.visible = false;
            }

            if (winBooks && winBag && winMap && winTreadmill && winFile && winOpponents) {
                sprite_checklist.visible = false;
                img_check1.visible = false;
                img_check2.visible = false;
                img_check3.visible = false;
                img_check4.visible = false;
                img_check5.visible = false;
                img_check6.visible = false;
                sprite_checklistW.setDepth(111).setInteractive();
                this.input.setDraggable(sprite_checklistW);
            }
            //var sprite_checklist = this.add.sprite(860, 160, 'imgChecklist').setOrigin(0);

            var sprite_flag1 = this.add.sprite(1200, 200, 'imgBoardFlag1').setOrigin(0).setInteractive();
            var sprite_run1 = this.add.sprite(1300, 200, 'imgBoardRun1').setOrigin(0).setInteractive();
            var sprite_run2 = this.add.sprite(440, 595, 'imgBoardRun2').setOrigin(0).setInteractive();
            var sprite_run3 = this.add.sprite(880, 600, 'imgBoardRun3').setOrigin(0).setInteractive();
            var sprite_run4 = this.add.sprite(940, 235, 'imgBoardRun4').setOrigin(0).setInteractive();
            var sprite_run5 = this.add.sprite(1410, 580, 'imgBoardRun5').setOrigin(0).setInteractive();
            var sprite_ball1 = this.add.sprite(790, 370, 'imgBall').setOrigin(0).setInteractive();
            var sprite_ball2 = this.add.sprite(620, 620, 'imgBall').setOrigin(0).setInteractive();
            var sprite_ball3 = this.add.sprite(665, 605, 'imgBall').setOrigin(0).setInteractive();
            var sprite_ball4 = this.add.sprite(630, 570, 'imgBall').setOrigin(0).setInteractive();

            var sprite_list4 = this.add.sprite(list4XY[0], list4XY[1], 'imgList4').setOrigin(0).setScale(0.1).setInteractive();

            var sprite_list1 = this.add.sprite(list1XY[0], list1XY[1], 'imgList1').setOrigin(0).setScale(0.1).setInteractive();
            var sprite_list2 = this.add.sprite(list2XY[0], list2XY[1], 'imgList2').setOrigin(0).setScale(0.1).setInteractive();
            var sprite_list3 = this.add.sprite(list3XY[0], list3XY[1], 'imgList3').setOrigin(0).setScale(0.1).setInteractive();
            var sprite_listFull = this.add.sprite(1050, 485, 'imgListFull').setOrigin(0).setScale(0.22).setInteractive();
            sprite_list1.setName('sList1');
            sprite_list2.setName('sList2');
            sprite_list3.setName('sList3');
            sprite_list4.setName('sList4');
            sprite_list1.visible = false;
            sprite_list2.visible = false;
            sprite_list3.visible = false;
            sprite_listFull.visible = false;

            if (listP1Ok) sprite_list1.visible = true;
            if (listP2Ok) sprite_list2.visible = true;
            if (listP3Ok) sprite_list3.visible = true;
            if (listOk) {
                sprite_list1.visible = false;
                sprite_list2.visible = false;
                sprite_list3.visible = false;
                sprite_list4.visible = false;
                sprite_listFull.visible = true;
            }
            this.add.image(1182, 772, 'imgLamp').setOrigin(0).setScale(1.08);

            this.input.setDraggable(sprite_flag1);
            this.input.setDraggable(sprite_run1);
            this.input.setDraggable(sprite_run2);
            this.input.setDraggable(sprite_run3);
            this.input.setDraggable(sprite_run4);
            this.input.setDraggable(sprite_run5);

            this.input.setDraggable(sprite_ball1);
            this.input.setDraggable(sprite_ball2);
            this.input.setDraggable(sprite_ball3);
            this.input.setDraggable(sprite_ball4);

            this.input.setDraggable(sprite_list1);
            this.input.setDraggable(sprite_list2);
            this.input.setDraggable(sprite_list3);
            this.input.setDraggable(sprite_list4);

            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_board = new Phaser.Geom.Polygon([290, 0, 1690, 0, 1650, 860, 330, 860]);
            var plgn_wardrobe = new Phaser.Geom.Polygon([1630, 0, 1920, 0, 1920, 920, 1630, 920]);
            var plgn_с1 = new Phaser.Geom.Polygon([1050, 550, 1450, 550, 1450, 580, 1050, 580]);
            var plgn_с2 = new Phaser.Geom.Polygon([1050, 580, 1450, 580, 1450, 610, 1050, 610]);
            var plgn_с3 = new Phaser.Geom.Polygon([1050, 610, 1450, 610, 1450, 640, 1050, 640]);
            var plgn_с4 = new Phaser.Geom.Polygon([1050, 640, 1450, 640, 1450, 670, 1050, 670]);
            var plgn_с5 = new Phaser.Geom.Polygon([1050, 670, 1450, 670, 1450, 700, 1050, 700]);
            var plgn_с6 = new Phaser.Geom.Polygon([1050, 700, 1450, 700, 1450, 730, 1050, 730]);
            var plgn_с7 = new Phaser.Geom.Polygon([1050, 730, 1450, 730, 1450, 760, 1050, 760]);

            var groupC1 = this.add.group();
            var groupC2 = this.add.group();
            var groupC3 = this.add.group();
            var groupC4 = this.add.group();
            var groupC5 = this.add.group();
            var groupC6 = this.add.group();
            var groupC7 = this.add.group();
            for (var i = 1; i <= 12; i++) {
                groupC1.create(1130, 520, 'imgCountry' + i).setOrigin(0).setScale(0.12);
                groupC2.create(1130, 550, 'imgCountry' + i).setOrigin(0).setScale(0.12);
                groupC3.create(1130, 580, 'imgCountry' + i).setOrigin(0).setScale(0.12);
                groupC4.create(1130, 610, 'imgCountry' + i).setOrigin(0).setScale(0.12);
                groupC5.create(1130, 640, 'imgCountry' + i).setOrigin(0).setScale(0.12);
                groupC6.create(1130, 670, 'imgCountry' + i).setOrigin(0).setScale(0.12);
                groupC7.create(1130, 700, 'imgCountry' + i).setOrigin(0).setScale(0.12);
            }
            var childC1 = groupC1.getChildren();
            var childC2 = groupC2.getChildren();
            var childC3 = groupC3.getChildren();
            var childC4 = groupC4.getChildren();
            var childC5 = groupC5.getChildren();
            var childC6 = groupC6.getChildren();
            var childC7 = groupC7.getChildren();
            for (var i = 0; i < 12; i++) {
                childC1[i].visible = false;
                childC2[i].visible = false;
                childC3[i].visible = false;
                childC4[i].visible = false;
                childC5[i].visible = false;
                childC6[i].visible = false;
                childC7[i].visible = false;
            }
            if (countries[0]) childC1[countries[0] - 1].visible = true;
            if (countries[1]) childC2[countries[1] - 1].visible = true;
            if (countries[2]) childC3[countries[2] - 1].visible = true;
            if (countries[3]) childC4[countries[3] - 1].visible = true;
            if (countries[4]) childC5[countries[4] - 1].visible = true;
            if (countries[5]) childC6[countries[5] - 1].visible = true;
            if (countries[6]) childC7[countries[6] - 1].visible = true;
            var sprite_с1 = this.add.sprite(0, 0);
            var sprite_с2 = this.add.sprite(0, 0);
            var sprite_с3 = this.add.sprite(0, 0);
            var sprite_с4 = this.add.sprite(0, 0);
            var sprite_с5 = this.add.sprite(0, 0);
            var sprite_с6 = this.add.sprite(0, 0);
            var sprite_с7 = this.add.sprite(0, 0);
            if (listOk) {
                sprite_с1.setInteractive(plgn_с1, Phaser.Geom.Polygon.Contains);
                sprite_с2.setInteractive(plgn_с2, Phaser.Geom.Polygon.Contains);
                sprite_с3.setInteractive(plgn_с3, Phaser.Geom.Polygon.Contains);
                sprite_с4.setInteractive(plgn_с4, Phaser.Geom.Polygon.Contains);
                sprite_с5.setInteractive(plgn_с5, Phaser.Geom.Polygon.Contains);
                sprite_с6.setInteractive(plgn_с6, Phaser.Geom.Polygon.Contains);
                sprite_с7.setInteractive(plgn_с7, Phaser.Geom.Polygon.Contains);
            }



            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_wardrobe.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_board.setInteractive(plgn_board, Phaser.Geom.Polygon.Contains);
            sprite_wardrobe.setInteractive(plgn_wardrobe, Phaser.Geom.Polygon.Contains);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                this.scene.start('DeskScene');
            }, this);

            sprite_wardrobe.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('WardrobeScene');
            }, this);

            sprite_checklist.on('pointerdown', function (pointer, gameObject) {
                if (winBooks && winBag && winMap && winTreadmill && winFile && winOpponents) {
                    sprite_checklist.visible = false;
                    img_check1.visible = false;
                    img_check2.visible = false;
                    img_check3.visible = false;
                    img_check4.visible = false;
                    img_check5.visible = false;
                    img_check6.visible = false;
                    sprite_checklistW.setDepth(111).setInteractive();
                    this.input.setDraggable(sprite_checklistW);
                    fxPage = this.sound.add('mp3Mark2');
                    fxPage.play();
                }
            }, this);

            sprite_с1.on('pointerdown', function (pointer, gameObject) {
                countries[0]++;
                if (countries[0] >= 12) countries[0] = 1;
                for (var i = 0; i < 12; i++) {
                    childC1[i].visible = false;
                }
                childC1[countries[0] - 1].visible = true;

                fxPage = this.sound.add('mp3Mark3');
                fxPage.play();

                if (countries[0] == 4 && countries[1] == 2 && countries[2] == 5 && countries[3] == 7 && countries[4] == 1 && countries[5] == 6 && countries[6] == 3) {
                    winOpponents = true;
                    img_check6.visible = true;
                    fxPage = this.sound.add('mp3Mark1');
                    fxPage.play();
                    sprite_с1.disableInteractive();
                    sprite_с2.disableInteractive();
                    sprite_с3.disableInteractive();
                    sprite_с4.disableInteractive();
                    sprite_с5.disableInteractive();
                    sprite_с6.disableInteractive();
                    sprite_с7.disableInteractive();

                }
            }, this);

            sprite_с2.on('pointerdown', function (pointer, gameobject) {
                countries[1]++;
                if (countries[1] >= 12) countries[1] = 1;
                for (var i = 0; i < 12; i++) {
                    childC2[i].visible = false;
                }
                childC2[countries[1] - 1].visible = true;

                fxPage = this.sound.add('mp3Mark3');
                fxPage.play();

                if (countries[0] == 4 && countries[1] == 2 && countries[2] == 5 && countries[3] == 7 && countries[4] == 1 && countries[5] == 6 && countries[6] == 3) {
                    winOpponents = true;
                    img_check6.visible = true;
                    fxPage = this.sound.add('mp3Mark1');
                    fxPage.play();
                    sprite_с1.disableInteractive();
                    sprite_с2.disableInteractive();
                    sprite_с3.disableInteractive();
                    sprite_с4.disableInteractive();
                    sprite_с5.disableInteractive();
                    sprite_с6.disableInteractive();
                    sprite_с7.disableInteractive();

                }
            }, this);

            sprite_с3.on('pointerdown', function (pointer, gameobject) {
                countries[2]++;
                if (countries[2] >= 12) countries[2] = 1;
                for (var i = 0; i < 12; i++) {
                    childC3[i].visible = false;
                }
                childC3[countries[2] - 1].visible = true;

                fxPage = this.sound.add('mp3Mark3');
                fxPage.play();

                if (countries[0] == 4 && countries[1] == 2 && countries[2] == 5 && countries[3] == 7 && countries[4] == 1 && countries[5] == 6 && countries[6] == 3) {
                    winOpponents = true;
                    img_check6.visible = true;
                    fxPage = this.sound.add('mp3Mark1');
                    fxPage.play();
                    sprite_с1.disableInteractive();
                    sprite_с2.disableInteractive();
                    sprite_с3.disableInteractive();
                    sprite_с4.disableInteractive();
                    sprite_с5.disableInteractive();
                    sprite_с6.disableInteractive();
                    sprite_с7.disableInteractive();

                }
            }, this);

            sprite_с4.on('pointerdown', function (pointer, gameobject) {
                countries[3]++;
                if (countries[3] >= 12) countries[3] = 1;
                for (var i = 0; i < 12; i++) {
                    childC4[i].visible = false;
                }
                childC4[countries[3] - 1].visible = true;

                fxPage = this.sound.add('mp3Mark3');
                fxPage.play();
                if (countries[0] == 4 && countries[1] == 2 && countries[2] == 5 && countries[3] == 7 && countries[4] == 1 && countries[5] == 6 && countries[6] == 3) {
                    winOpponents = true;
                    img_check6.visible = true;
                    fxPage = this.sound.add('mp3Mark1');
                    fxPage.play();
                    sprite_с1.disableInteractive();
                    sprite_с2.disableInteractive();
                    sprite_с3.disableInteractive();
                    sprite_с4.disableInteractive();
                    sprite_с5.disableInteractive();
                    sprite_с6.disableInteractive();
                    sprite_с7.disableInteractive();

                }
            }, this);

            sprite_с5.on('pointerdown', function (pointer, gameobject) {
                countries[4]++;
                if (countries[4] >= 12) countries[4] = 1;
                for (var i = 0; i < 12; i++) {
                    childC5[i].visible = false;
                }
                childC5[countries[4] - 1].visible = true;

                fxPage = this.sound.add('mp3Mark3');
                fxPage.play();

                if (countries[0] == 4 && countries[1] == 2 && countries[2] == 5 && countries[3] == 7 && countries[4] == 1 && countries[5] == 6 && countries[6] == 3) {
                    winOpponents = true;
                    img_check6.visible = true;
                    fxPage = this.sound.add('mp3Mark1');
                    fxPage.play();
                    sprite_с1.disableInteractive();
                    sprite_с2.disableInteractive();
                    sprite_с3.disableInteractive();
                    sprite_с4.disableInteractive();
                    sprite_с5.disableInteractive();
                    sprite_с6.disableInteractive();
                    sprite_с7.disableInteractive();

                }
            }, this);

            sprite_с6.on('pointerdown', function (pointer, gameobject) {
                countries[5]++;
                if (countries[5] >= 12) countries[5] = 1;
                for (var i = 0; i < 12; i++) {
                    childC6[i].visible = false;
                }
                childC6[countries[5] - 1].visible = true;

                fxPage = this.sound.add('mp3Mark3');
                fxPage.play();

                if (countries[0] == 4 && countries[1] == 2 && countries[2] == 5 && countries[3] == 7 && countries[4] == 1 && countries[5] == 6 && countries[6] == 3) {
                    winOpponents = true;
                    img_check6.visible = true;
                    fxPage = this.sound.add('mp3Mark1');
                    fxPage.play();
                    sprite_с1.disableInteractive();
                    sprite_с2.disableInteractive();
                    sprite_с3.disableInteractive();
                    sprite_с4.disableInteractive();
                    sprite_с5.disableInteractive();
                    sprite_с6.disableInteractive();
                    sprite_с7.disableInteractive();

                }
            }, this);

            sprite_с7.on('pointerdown', function (pointer, gameobject) {
                countries[6]++;
                if (countries[6] >= 12) countries[6] = 1;
                for (var i = 0; i < 12; i++) {
                    childC7[i].visible = false;
                }
                childC7[countries[6] - 1].visible = true;

                fxPage = this.sound.add('mp3Mark3');
                fxPage.play();

                if (countries[0] == 4 && countries[1] == 2 && countries[2] == 5 && countries[3] == 7 && countries[4] == 1 && countries[5] == 6 && countries[6] == 3) {
                    winOpponents = true;
                    img_check6.visible = true;
                    fxPage = this.sound.add('mp3Mark1');
                    fxPage.play();
                    sprite_с1.disableInteractive();
                    sprite_с2.disableInteractive();
                    sprite_с3.disableInteractive();
                    sprite_с4.disableInteractive();
                    sprite_с5.disableInteractive();
                    sprite_с6.disableInteractive();
                    sprite_с7.disableInteractive();

                }
            }, this);


            this.input.on('drag', function (pointer, gameObject, dragX, dragY) {
                if (dragX > 400 && dragX < 1500) {
                    gameObject.x = dragX;
                }

                if (dragY > 150 && dragY < 850) {
                    gameObject.y = dragY;
                }
            });

            this.input.on('dragend', function (pointer, gameObject, dragX, dragY) {
                if (!('sList1' == gameObject.name) && !('sList2' == gameObject.name) && !('sList3' == gameObject.name) && !('sList4' == gameObject.name) && !('sChecklistW' == gameObject.name)) {
                    gameObject.x = gameObject.input.dragStartX;
                    gameObject.y = gameObject.input.dragStartY;
                }
                if ('sList1' == gameObject.name) {
                    list1XY[0] = gameObject.x;
                    list1XY[1] = gameObject.y;
                }
                if ('sList2' == gameObject.name) {
                    list2XY[0] = gameObject.x;
                    list2XY[1] = gameObject.y;
                }
                if ('sList3' == gameObject.name) {
                    list3XY[0] = gameObject.x;
                    list3XY[1] = gameObject.y;
                }
                if ('sList4' == gameObject.name) {
                    list4XY[0] = gameObject.x;
                    list4XY[1] = gameObject.y;
                }

            });

            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });
        }

        function createShelfScene() {

            this.add.image(0, 0, 'imgShelf').setOrigin(0);
            this.add.image(615, 580, 'imgBttnOff').setOrigin(0);
            this.add.image(750, 580, 'imgBttnOff').setOrigin(0);
            this.add.image(940, 580, 'imgBttnOff').setOrigin(0);
            this.add.image(1075, 580, 'imgBttnOff').setOrigin(0);
            this.add.image(1210, 580, 'imgBttnOff').setOrigin(0);
            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_shelf = this.add.sprite(0, 0);

            var sprite_bttn1 = this.add.sprite(615, 583, 'imgBttnOn').setOrigin(0).setInteractive();
            var sprite_bttn2 = this.add.sprite(750, 583, 'imgBttnOn').setOrigin(0).setInteractive();
            var sprite_bttn3 = this.add.sprite(940, 583, 'imgBttnOn').setOrigin(0).setInteractive();
            var sprite_bttn4 = this.add.sprite(1075, 583, 'imgBttnOn').setOrigin(0).setInteractive();
            var sprite_bttn5 = this.add.sprite(1210, 583, 'imgBttnOn').setOrigin(0).setInteractive();

            var pass = [0, 0, 0, 0, 0];

            var groupD1 = this.add.group();
            for (var i = 0; i <= 9; i++) {
                groupD1.create(640, 430, 'imgShelfD' + i).setOrigin(0);
            }
            var childD1 = groupD1.getChildren();
            for (var i = 0; i < 10; i++) {
                childD1[i].visible = false;
            }
            childD1[pass[0]].visible = true;

            var groupD2 = this.add.group();
            for (var i = 0; i <= 9; i++) {
                groupD2.create(775, 430, 'imgShelfD' + i).setOrigin(0);
            }
            var childD2 = groupD2.getChildren();
            for (var i = 0; i < 10; i++) {
                childD2[i].visible = false;
            }
            childD2[pass[1]].visible = true;

            var groupD3 = this.add.group();
            for (var i = 0; i <= 9; i++) {
                groupD3.create(965, 430, 'imgShelfD' + i).setOrigin(0);
            }
            var childD3 = groupD3.getChildren();
            for (var i = 0; i < 10; i++) {
                childD3[i].visible = false;
            }
            childD3[pass[2]].visible = true;

            var groupD4 = this.add.group();
            for (var i = 0; i <= 9; i++) {
                groupD4.create(1100, 430, 'imgShelfD' + i).setOrigin(0);
            }
            var childD4 = groupD4.getChildren();
            for (var i = 0; i < 10; i++) {
                childD4[i].visible = false;
            }
            childD4[pass[3]].visible = true;

            var groupD5 = this.add.group();
            for (var i = 0; i <= 9; i++) {
                groupD5.create(1235, 430, 'imgShelfD' + i).setOrigin(0);
            }
            var childD5 = groupD5.getChildren();
            for (var i = 0; i < 10; i++) {
                childD5[i].visible = false;
            }
            childD5[pass[4]].visible = true;



            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_shelf = new Phaser.Geom.Polygon([550, 320, 1370, 320, 1370, 740, 550, 740]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_shelf.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_shelf.setInteractive(plgn_shelf, Phaser.Geom.Polygon.Contains);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                this.scene.start('DeskScene');
            }, this);

            sprite_bttn1.on('pointerdown', function (pointer, gameObject) {
                pass[0]++;
                if (pass[0] >= 10) pass[0] = 0;

                for (var i = 0; i < 10; i++) {
                    childD1[i].visible = false;
                }

                childD1[pass[0]].visible = true;

                sprite_bttn1.visible = false;
                timedEvent = this.time.addEvent({
                    delay: 200, callback: () => {

                        sprite_bttn1.visible = true;

                    }, callbackScope: this, repeat: 0, startAt: 0
                });
                fxBttn = this.sound.add('mp3shelfBttn');
                fxBttn.play();

                if (pass[0] == 4 && pass[1] == 2 && pass[2] == 1 && pass[3] == 9 && pass[4] == 5) {
                    fxUnlock = this.sound.add('mp3Unlock');
                    fxUnlock.play();
                    winShelf = true;
                    timedEvent = this.time.addEvent({
                        delay: 1000, callback: () => {
                            this.scene.start('DeskScene');
                        }, callbackScope: this, repeat: 0, startAt: 0
                    });
                }
            }, this);

            sprite_bttn2.on('pointerdown', function (pointer, gameObject) {
                pass[1]++;
                if (pass[1] >= 10) pass[1] = 0;

                for (var i = 0; i < 10; i++) {
                    childD2[i].visible = false;
                }

                childD2[pass[1]].visible = true;

                sprite_bttn2.visible = false;
                timedEvent = this.time.addEvent({
                    delay: 200, callback: () => {

                        sprite_bttn2.visible = true;

                    }, callbackScope: this, repeat: 0, startAt: 0
                });
                fxBttn = this.sound.add('mp3shelfBttn');
                fxBttn.play();

                if (pass[0] == 4 && pass[1] == 2 && pass[2] == 1 && pass[3] == 9 && pass[4] == 5) {
                    fxUnlock = this.sound.add('mp3Unlock');
                    fxUnlock.play();
                    winShelf = true;
                    timedEvent = this.time.addEvent({
                        delay: 1000, callback: () => {
                            this.scene.start('DeskScene');
                        }, callbackScope: this, repeat: 0, startAt: 0
                    });
                }
            }, this);

            sprite_bttn3.on('pointerdown', function (pointer, gameObject) {
                pass[2]++;
                if (pass[2] >= 10) pass[2] = 0;

                for (var i = 0; i < 10; i++) {
                    childD3[i].visible = false;
                }

                childD3[pass[2]].visible = true;

                sprite_bttn3.visible = false;
                timedEvent = this.time.addEvent({
                    delay: 200, callback: () => {

                        sprite_bttn3.visible = true;

                    }, callbackScope: this, repeat: 0, startAt: 0
                });
                fxBttn = this.sound.add('mp3shelfBttn');
                fxBttn.play();

                if (pass[0] == 4 && pass[1] == 2 && pass[2] == 1 && pass[3] == 9 && pass[4] == 5) {
                    fxUnlock = this.sound.add('mp3Unlock');
                    fxUnlock.play();
                    winShelf = true;
                    timedEvent = this.time.addEvent({
                        delay: 1000, callback: () => {
                            this.scene.start('DeskScene');
                        }, callbackScope: this, repeat: 0, startAt: 0
                    });
                }
            }, this);

            sprite_bttn4.on('pointerdown', function (pointer, gameObject) {
                pass[3]++;
                if (pass[3] >= 10) pass[3] = 0;

                for (var i = 0; i < 10; i++) {
                    childD4[i].visible = false;
                }

                childD4[pass[3]].visible = true;

                sprite_bttn4.visible = false;
                timedEvent = this.time.addEvent({
                    delay: 200, callback: () => {

                        sprite_bttn4.visible = true;

                    }, callbackScope: this, repeat: 0, startAt: 0
                });
                fxBttn = this.sound.add('mp3shelfBttn');
                fxBttn.play();

                if (pass[0] == 4 && pass[1] == 2 && pass[2] == 1 && pass[3] == 9 && pass[4] == 5) {
                    fxUnlock = this.sound.add('mp3Unlock');
                    fxUnlock.play();
                    winShelf = true;
                    timedEvent = this.time.addEvent({
                        delay: 1000, callback: () => {
                            this.scene.start('DeskScene');
                        }, callbackScope: this, repeat: 0, startAt: 0
                    });
                }
            }, this);

            sprite_bttn5.on('pointerdown', function (pointer, gameObject) {
                pass[4]++;
                if (pass[4] >= 10) pass[4] = 0;

                for (var i = 0; i < 10; i++) {
                    childD5[i].visible = false;
                }

                childD5[pass[4]].visible = true;

                sprite_bttn5.visible = false;
                timedEvent = this.time.addEvent({
                    delay: 200, callback: () => {

                        sprite_bttn5.visible = true;

                    }, callbackScope: this, repeat: 0, startAt: 0
                });
                fxBttn = this.sound.add('mp3shelfBttn');
                fxBttn.play();

                if (pass[0] == 4 && pass[1] == 2 && pass[2] == 1 && pass[3] == 9 && pass[4] == 5) {
                    fxUnlock = this.sound.add('mp3Unlock');
                    fxUnlock.play();
                    winShelf = true;
                    timedEvent = this.time.addEvent({
                        delay: 1000, callback: () => {
                            this.scene.start('DeskScene');
                        }, callbackScope: this, repeat: 0, startAt: 0
                    });
                }
            }, this);

            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });
        }

        function createLaptopScene() {

            this.add.image(0, 0, 'imgLaptop').setOrigin(0);

            var imgPower = this.add.image(975, 910, 'imgPowerScene3').setOrigin(0);
            var imgDesktop1 = this.add.image(449, 197, 'imgLaptop1Scene3').setOrigin(0);

            imgDesktop1.visible = false;

            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_laptop = this.add.sprite(0, 0);
            var sprite_power = this.add.sprite(0, 0);
            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_laptop = new Phaser.Geom.Polygon([320, 100, 1650, 100, 1650, 920, 320, 920]);
            var plgn_power = new Phaser.Geom.Polygon([880, 890, 1060, 890, 1060, 970, 880, 970]);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();
            var password = this.add.dom(1000, 600).createFromCache('nameform');
            password.visible = false;

            this.input.topOnly = true;

            if (laptopOn) {
                imgPower.visible = true;
                imgDesktop1.visible = true;
                password.visible = true;
                password.addListener('click');
            } else {
                imgPower.visible = false;
                sprite_power.setInteractive(plgn_power, Phaser.Geom.Polygon.Contains);
            }

            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_laptop.setInteractive(plgn_laptop, Phaser.Geom.Polygon.Contains);

            password.on('click', function (event) {
                if (event.target.name === 'playButton') {

                    var textPass = this.getChildByName('nameField');


                    if ('records' === textPass.value.toLowerCase()) {
                        recordsOn = true;
                        this.removeListener('click');
                        password.visible = false;
                        textPass.value = '';

                    } else {
                        textPass.value = '';
                    }

                }


            });


            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                this.scene.start('DeskScene');
            }, this);

            sprite_power.on('pointerdown', function (pointer, gameObject) {
                if (!laptopOn) {
                    sprite_power.disableInteractive();
                    laptopOn = true;
                    imgPower.visible = true;
                    fxOn = this.sound.add('mp3Laptop');
                    fxOn.play();
                    fxOn = this.sound.add('mp3Laptop2');
                    fxOn.play();

                    timedEvent = this.time.addEvent({
                        delay: 1000, callback: () => {
                            imgDesktop1.visible = true;
                            password.visible = true;
                            password.addListener('click');
                        }, callbackScope: this, repeat: 0, startAt: 0
                    });
                }
            }, this);

            sprite_laptop.on('pointerdown', function (pointer, gameObject) {
                if (recordsOn) {
                    this.scene.start('Laptop2Scene');
                    fxOn = this.sound.add('mp3Laptop3');
                    fxOn.play();
                }
            }, this);


            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });
        }

        function createLaptop2Scene() {

            this.add.image(0, 0, 'imgLaptop').setOrigin(0);
            this.add.image(975, 910, 'imgPowerScene3').setOrigin(0);
            this.add.image(449, 197, 'imgLaptop2Scene3').setOrigin(0);
            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
            var imgLock = this.add.image(1460, 270, 'imgLockScene3').setOrigin(0);
            var imgPrinter = this.add.image(570, 470, 'imgPrinterScene3').setOrigin(0);
            if (winFile) imgLock.visible = false;
            if (winPrinter) imgPrinter.visible = false;
            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_laptop = this.add.sprite(0, 0);

            var sprite_youtube = this.add.sprite(0, 0);
            var sprite_insta = this.add.sprite(0, 0);
            var sprite_printer = this.add.sprite(0, 0);
            var sprite_file = this.add.sprite(0, 0);

            var sprite_printerMessage = this.add.sprite(1000, 540, 'imgPrinterMessageScene3');
            var sprite_printerOk = this.add.sprite(1000, 605, 'imgPrinterOk');
            var sprite_printerL = this.add.sprite(868, 550, 'imgPrinterL');
            var sprite_printerR = this.add.sprite(1133, 554, 'imgPrinterR');

            sprite_printerMessage.visible = false;
            sprite_printerOk.visible = false;
            sprite_printerL.visible = false;
            sprite_printerR.visible = false;

            var sprite_fileMessage = this.add.sprite(1000, 540, 'imgFileMessageScene3');
            sprite_fileMessage.visible = false;

            var sprite_L1I = this.add.sprite(0, 0);
            var sprite_L1D = this.add.sprite(0, 0);
            var sprite_L2I = this.add.sprite(0, 0);
            var sprite_L2D = this.add.sprite(0, 0);
            var sprite_L3I = this.add.sprite(0, 0);
            var sprite_L3D = this.add.sprite(0, 0);

            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_laptop = new Phaser.Geom.Polygon([320, 100, 1650, 100, 1650, 920, 320, 920]);

            var plgn_youtube = new Phaser.Geom.Polygon([520, 230, 600, 230, 600, 310, 520, 310]);
            var plgn_insta = new Phaser.Geom.Polygon([520, 310, 600, 310, 600, 405, 520, 405]);
            var plgn_printer = new Phaser.Geom.Polygon([520, 405, 600, 405, 600, 510, 520, 510]);
            var plgn_file = new Phaser.Geom.Polygon([1440, 230, 1520, 230, 1520, 320, 1440, 320]);

            var plgn_L1I = new Phaser.Geom.Polygon([870, 500, 940, 500, 940, 550, 870, 550]);
            var plgn_L1D = new Phaser.Geom.Polygon([870, 600, 940, 600, 940, 650, 870, 650]);
            var plgn_L2I = new Phaser.Geom.Polygon([970, 500, 1040, 500, 1040, 550, 970, 550]);
            var plgn_L2D = new Phaser.Geom.Polygon([970, 600, 1040, 600, 1040, 650, 970, 650]);
            var plgn_L3I = new Phaser.Geom.Polygon([1070, 500, 1140, 500, 1140, 550, 1070, 550]);
            var plgn_L3D = new Phaser.Geom.Polygon([1070, 600, 1140, 600, 1140, 650, 1070, 650]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_power.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            printerCount = this.add.text(990, 545, '', { fill: '#1B2631', font: '20px Courier' }).setDepth(1);

            fileL1 = this.add.text(883, 552, '', { fill: '#212F3C', font: '64px Courier' }).setDepth(1);
            fileL2 = this.add.text(982, 552, '', { fill: '#212F3C', font: '64px Courier' }).setDepth(1);
            fileL3 = this.add.text(1081, 552, '', { fill: '#212F3C', font: '64px Courier' }).setDepth(1);

            printerCount.visible = false;
            fileL1.visible = false;
            fileL2.visible = false;
            fileL3.visible = false;

            this.input.mouse.disableContextMenu();


            this.input.topOnly = true;

            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_laptop.setInteractive(plgn_laptop, Phaser.Geom.Polygon.Contains);
            sprite_youtube.setInteractive(plgn_youtube, Phaser.Geom.Polygon.Contains);
            sprite_insta.setInteractive(plgn_insta, Phaser.Geom.Polygon.Contains);
            sprite_printer.setInteractive(plgn_printer, Phaser.Geom.Polygon.Contains);
            sprite_file.setInteractive(plgn_file, Phaser.Geom.Polygon.Contains);

            sprite_L1I.setInteractive(plgn_L1I, Phaser.Geom.Polygon.Contains);
            sprite_L1D.setInteractive(plgn_L1D, Phaser.Geom.Polygon.Contains);
            sprite_L2I.setInteractive(plgn_L2I, Phaser.Geom.Polygon.Contains);
            sprite_L2D.setInteractive(plgn_L2D, Phaser.Geom.Polygon.Contains);
            sprite_L3I.setInteractive(plgn_L3I, Phaser.Geom.Polygon.Contains);
            sprite_L3D.setInteractive(plgn_L3D, Phaser.Geom.Polygon.Contains);
            sprite_L1I.disableInteractive();
            sprite_L1D.disableInteractive();
            sprite_L2I.disableInteractive();
            sprite_L2D.disableInteractive();
            sprite_L3I.disableInteractive();
            sprite_L3D.disableInteractive();

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                this.scene.start('DeskScene');
            }, this);

            sprite_laptop.on('pointerdown', function (pointer, gameObject) {
                sprite_printerMessage.visible = false;
                sprite_fileMessage.visible = false;

                sprite_printerMessage.disableInteractive();
                sprite_fileMessage.disableInteractive();
                printerCount.visible = false;
                fileL1.visible = false;
                fileL2.visible = false;
                fileL3.visible = false;

                sprite_L1I.disableInteractive();
                sprite_L1D.disableInteractive();
                sprite_L2I.disableInteractive();
                sprite_L2D.disableInteractive();
                sprite_L3I.disableInteractive();
                sprite_L3D.disableInteractive();

                sprite_printerOk.visible = false;
                sprite_printerL.visible = false;
                sprite_printerR.visible = false;
                sprite_printerOk.disableInteractive();
                sprite_printerL.disableInteractive();
                sprite_printerR.disableInteractive();

            }, this);

            sprite_youtube.on('pointerdown', function (pointer, gameObject) {
                window.open(youtubeLink);
                // window.location.href = 'https://youtube.com'
            }, this);

            sprite_insta.on('pointerdown', function (pointer, gameObject) {
                window.open(instaLink);
                // window.location.href = 'https://youtube.com'
            }, this);

            sprite_printer.on('pointerdown', function (pointer, gameObject) {
                if (!winPrinter) {
                    sprite_printerMessage.visible = true;
                    sprite_printerMessage.setInteractive();
                    sprite_fileMessage.visible = false;
                    sprite_fileMessage.disableInteractive();
                    printerCount.visible = true;
                    fileL1.visible = false;
                    fileL2.visible = false;
                    fileL3.visible = false;
                    //printerPass += 50;
                    sprite_printerOk.visible = true;
                    sprite_printerL.visible = true;
                    sprite_printerR.visible = true;
                    sprite_printerOk.setInteractive();
                    sprite_printerL.setInteractive();
                    sprite_printerR.setInteractive();

                    sprite_L1I.disableInteractive();
                    sprite_L1D.disableInteractive();
                    sprite_L2I.disableInteractive();
                    sprite_L2D.disableInteractive();
                    sprite_L3I.disableInteractive();
                    sprite_L3D.disableInteractive();
                }

            }, this);

            sprite_file.on('pointerdown', function (pointer, gameObject) {
                if (!winFile) {
                    sprite_fileMessage.visible = true;
                    sprite_fileMessage.setInteractive();
                    sprite_printerMessage.visible = false;
                    sprite_printerMessage.disableInteractive();
                    printerCount.visible = false;
                    fileL1.visible = true;
                    fileL2.visible = true;
                    fileL3.visible = true;

                    sprite_printerOk.visible = false;
                    sprite_printerL.visible = false;
                    sprite_printerR.visible = false;
                    sprite_printerOk.disableInteractive();
                    sprite_printerL.disableInteractive();
                    sprite_printerR.disableInteractive();

                    sprite_L1I.setInteractive();
                    sprite_L1D.setInteractive();
                    sprite_L2I.setInteractive();
                    sprite_L2D.setInteractive();
                    sprite_L3I.setInteractive();
                    sprite_L3D.setInteractive();
                } else {
                    this.scene.start('Laptop3Scene')
                }


            }, this);

            sprite_L1I.on('pointerdown', function (pointer, gameObject) {
                fileL1Pass++;
                if (fileL1Pass == 26) fileL1Pass = 0;
                fxOn = this.sound.add('mp3AppBttn');
                fxOn.play();
                if (fileL1Pass == 17 && fileL2Pass == 20 && fileL3Pass == 13) {
                    winFile = true;
                    sprite_L1I.disableInteractive();
                    sprite_L1D.disableInteractive();
                    sprite_L2I.disableInteractive();
                    sprite_L2D.disableInteractive();
                    sprite_L3I.disableInteractive();
                    sprite_L3D.disableInteractive();
                    timedEvent = this.time.addEvent({
                        delay: 500, callback: () => {

                            fxPage = this.sound.add('mp3Mark1');
                            fxPage.play();

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 1250, callback: () => {

                            imgLock.visible = false;

                            sprite_fileMessage.visible = false;
                            sprite_fileMessage.disableInteractive();
                            fileL1.visible = false;
                            fileL2.visible = false;
                            fileL3.visible = false;

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });



                }
            }, this);
            sprite_L1D.on('pointerdown', function (pointer, gameObject) {
                fileL1Pass--;
                if (fileL1Pass == -1) fileL1Pass = 25;
                fxOn = this.sound.add('mp3AppBttn');
                fxOn.play();
                if (fileL1Pass == 17 && fileL2Pass == 20 && fileL3Pass == 13) {
                    winFile = true;
                    sprite_L1I.disableInteractive();
                    sprite_L1D.disableInteractive();
                    sprite_L2I.disableInteractive();
                    sprite_L2D.disableInteractive();
                    sprite_L3I.disableInteractive();
                    sprite_L3D.disableInteractive();
                    timedEvent = this.time.addEvent({
                        delay: 500, callback: () => {

                            fxPage = this.sound.add('mp3Mark1');
                            fxPage.play();

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 1250, callback: () => {

                            imgLock.visible = false;

                            sprite_fileMessage.visible = false;
                            sprite_fileMessage.disableInteractive();
                            fileL1.visible = false;
                            fileL2.visible = false;
                            fileL3.visible = false;

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });



                }

            }, this);

            sprite_L2I.on('pointerdown', function (pointer, gameObject) {
                fileL2Pass++;
                if (fileL2Pass == 26) fileL2Pass = 0;
                fxOn = this.sound.add('mp3AppBttn');
                fxOn.play();
                if (fileL1Pass == 17 && fileL2Pass == 20 && fileL3Pass == 13) {
                    winFile = true;
                    sprite_L1I.disableInteractive();
                    sprite_L1D.disableInteractive();
                    sprite_L2I.disableInteractive();
                    sprite_L2D.disableInteractive();
                    sprite_L3I.disableInteractive();
                    sprite_L3D.disableInteractive();
                    timedEvent = this.time.addEvent({
                        delay: 500, callback: () => {

                            fxPage = this.sound.add('mp3Mark1');
                            fxPage.play();

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 1250, callback: () => {

                            imgLock.visible = false;

                            sprite_fileMessage.visible = false;
                            sprite_fileMessage.disableInteractive();
                            fileL1.visible = false;
                            fileL2.visible = false;
                            fileL3.visible = false;

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });



                }

            }, this);
            sprite_L2D.on('pointerdown', function (pointer, gameObject) {
                fileL2Pass--;
                if (fileL2Pass == -1) fileL2Pass = 25;
                fxOn = this.sound.add('mp3AppBttn');
                fxOn.play();
                if (fileL1Pass == 17 && fileL2Pass == 20 && fileL3Pass == 13) {
                    winFile = true;
                    sprite_L1I.disableInteractive();
                    sprite_L1D.disableInteractive();
                    sprite_L2I.disableInteractive();
                    sprite_L2D.disableInteractive();
                    sprite_L3I.disableInteractive();
                    sprite_L3D.disableInteractive();
                    timedEvent = this.time.addEvent({
                        delay: 500, callback: () => {

                            fxPage = this.sound.add('mp3Mark1');
                            fxPage.play();

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 1250, callback: () => {

                            imgLock.visible = false;

                            sprite_fileMessage.visible = false;
                            sprite_fileMessage.disableInteractive();
                            fileL1.visible = false;
                            fileL2.visible = false;
                            fileL3.visible = false;

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });



                }

            }, this);

            sprite_L3I.on('pointerdown', function (pointer, gameObject) {
                fileL3Pass++;
                if (fileL3Pass == 26) fileL3Pass = 0;
                fxOn = this.sound.add('mp3AppBttn');
                fxOn.play();
                if (fileL1Pass == 17 && fileL2Pass == 20 && fileL3Pass == 13) {
                    winFile = true;
                    sprite_L1I.disableInteractive();
                    sprite_L1D.disableInteractive();
                    sprite_L2I.disableInteractive();
                    sprite_L2D.disableInteractive();
                    sprite_L3I.disableInteractive();
                    sprite_L3D.disableInteractive();
                    timedEvent = this.time.addEvent({
                        delay: 500, callback: () => {

                            fxPage = this.sound.add('mp3Mark1');
                            fxPage.play();

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 1250, callback: () => {

                            imgLock.visible = false;

                            sprite_fileMessage.visible = false;
                            sprite_fileMessage.disableInteractive();
                            fileL1.visible = false;
                            fileL2.visible = false;
                            fileL3.visible = false;

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });



                }

            }, this);
            sprite_L3D.on('pointerdown', function (pointer, gameObject) {
                fileL3Pass--;
                if (fileL3Pass == -1) fileL3Pass = 25;
                fxOn = this.sound.add('mp3AppBttn');
                fxOn.play();
                if (fileL1Pass == 17 && fileL2Pass == 20 && fileL3Pass == 13) {
                    winFile = true;
                    sprite_L1I.disableInteractive();
                    sprite_L1D.disableInteractive();
                    sprite_L2I.disableInteractive();
                    sprite_L2D.disableInteractive();
                    sprite_L3I.disableInteractive();
                    sprite_L3D.disableInteractive();
                    timedEvent = this.time.addEvent({
                        delay: 500, callback: () => {

                            fxPage = this.sound.add('mp3Mark1');
                            fxPage.play();

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                    timedEvent = this.time.addEvent({
                        delay: 1250, callback: () => {

                            imgLock.visible = false;

                            sprite_fileMessage.visible = false;
                            sprite_fileMessage.disableInteractive();
                            fileL1.visible = false;
                            fileL2.visible = false;
                            fileL3.visible = false;

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });



                }

            }, this);

            sprite_printerL.on('pointerdown', function (pointer, gameObject) {
                printerPass -= 15;
                if (printerPass <= 0) printerPass = 0;
                fxOn = this.sound.add('mp3AppBttn');
                fxOn.play();
            }, this);
            sprite_printerR.on('pointerdown', function (pointer, gameObject) {
                printerPass += 15;

                fxOn = this.sound.add('mp3AppBttn');
                fxOn.play();

            }, this);
            sprite_printerOk.on('pointerdown', function (pointer, gameObject) {
                if (printerPass == 885 || printerPass == 870) {
                    winPrinter = true;
                    imgPrinter.visible = false;
                    printerCount.visible = false;

                    if (paperOk) {
                        fxPrint = this.sound.add('mp3print');
                        fxPrint.play();
                        timedEvent = this.time.addEvent({
                            delay: 4000, callback: () => {

                                this.scene.start('DeskScene');

                            }, callbackScope: this, repeat: 0, startAt: 0
                        });
                    }

                }
                printerCount.visible = false;
                sprite_printerMessage.visible = false;
                sprite_printerOk.visible = false;
                sprite_printerL.visible = false;
                sprite_printerR.visible = false;
                fxOn = this.sound.add('mp3Laptop');
                fxOn.play();

            }, this);

            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });
        }

        function createLaptop3Scene() {

            this.add.image(0, 0, 'imgLaptop').setOrigin(0);
            this.add.image(975, 910, 'imgPowerScene3').setOrigin(0);
            this.add.image(449, 197, 'imgLaptop2Scene3').setOrigin(0);
            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_laptop = this.add.sprite(0, 0);
            var sprite_file = this.add.sprite(915, 500, 'imgLaptopFlag').setScale(1.5).setInteractive();
            var sprite_flag1 = this.add.sprite(619, 466, 'imgLaptopFlag1').setScale(1.5).setInteractive();
            var sprite_flag2 = this.add.sprite(614, 584, 'imgLaptopFlag2').setScale(1.5).setInteractive();
            var sprite_flag3 = this.add.sprite(900, 400, 'imgLaptopFlag3').setScale(1.5).setInteractive();
            var sprite_flag31 = this.add.sprite(885, 400, 'imgLaptopFlag3.1').setScale(0.6).setDepth(100);
            var sprite_flag4 = this.add.sprite(844, 529, 'imgLaptopFlag4').setScale(1.5).setInteractive();
            var sprite_flag5 = this.add.sprite(860, 642, 'imgLaptopFlag5').setScale(1.5).setInteractive();
            var sprite_flag6 = this.add.sprite(1036, 486, 'imgLaptopFlag6').setScale(1.5).setInteractive();
            var sprite_flag7 = this.add.sprite(1207, 533, 'imgLaptopFlag7').setScale(1.5).setInteractive();
            this.input.setDraggable(sprite_flag1);
            this.input.setDraggable(sprite_flag2);
            this.input.setDraggable(sprite_flag3);
            this.input.setDraggable(sprite_flag4);
            this.input.setDraggable(sprite_flag5);
            this.input.setDraggable(sprite_flag6);
            this.input.setDraggable(sprite_flag7);

            var plgn_mainLeft = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_laptop = new Phaser.Geom.Polygon([320, 100, 1650, 100, 1650, 920, 320, 920]);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();
            this.input.topOnly = true;
            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_laptop.setInteractive(plgn_laptop, Phaser.Geom.Polygon.Contains);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                this.scene.start('DeskScene');
            }, this);

            sprite_laptop.on('pointerdown', function (pointer, gameObject) {
                this.scene.start('Laptop2Scene')
            }, this);

            this.input.on('dragstart', function (pointer, gameObject) {
                depth++;
                gameObject.setDepth(depth);

            }, this);

            this.input.on('drag', function (pointer, gameObject, dragX, dragY) {

                if (dragX > 550 && dragX < 1250) {
                    gameObject.x = dragX;
                }

                if (dragY > 320 && dragY < 700) {
                    gameObject.y = dragY;
                }

            });


            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });
        }

        function createDeskScene() {

            imgSceneClosed = this.add.image(0, 0, 'imgDeskClosed').setOrigin(0);
            var imgDesktop1 = this.add.image(890, 200, 'imgLaptop1Scene2').setOrigin(0);
            var imgDesktop2 = this.add.image(890, 200, 'imgLaptop2Scene2').setOrigin(0);
            this.add.image(1745, 370, 'imgPrinterGreen').setOrigin(0);
            this.add.image(1715, 375, 'imgPrinterGreen').setOrigin(0);
            var imgPrinterRed1 = this.add.image(1745, 370, 'imgPrinterRed').setOrigin(0);
            var imgPrinterRed2 = this.add.image(1715, 375, 'imgPrinterRed').setOrigin(0);
            imgDesktop1.visible = false;
            imgDesktop2.visible = false;
            var sprite_hint = this.add.sprite(1835, 35, 'imgHint').setOrigin().setScale(1).setDepth(100).setInteractive();
            var img_hint = this.add.sprite(1835, 35, 'imgHintL').setOrigin().setScale(1).setDepth(100);
            img_hint.visible = false;
            var sprite_magazine = this.add.sprite(780, 510, 'imgMagazine').setOrigin().setScale(0.8).setInteractive();


            if (winPrinter) imgPrinterRed2.visible = false;
            if (paperOk) imgPrinterRed1.visible = false;

            if (laptopOn) {
                imgDesktop1.visible = true;
            }
            if (recordsOn) {
                imgDesktop1.visible = false;
                imgDesktop2.visible = true;
            }

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

            childDayH[(g_day - g_day % 10) / 10].visible = true;

            var groupDayL = this.add.group();
            for (var i = 0; i <= 9; i++) {
                groupDayL.create(861, 326, 'imgD' + i).setOrigin(0);
            }
            var childDayL = groupDayL.getChildren();
            for (var i = 0; i < 10; i++) {
                childDayL[i].visible = false;
            }
            childDayL[g_day % 10].visible = true;



            var imgSceneOpened = this.add.image(101, 700, 'imgDeskOpened').setOrigin(0);
            imgSceneOpened.visible = false;

            var sprite_mainLeft = this.add.sprite(0, 0);
            var sprite_board = this.add.sprite(0, 0);
            var sprite_shelf = this.add.sprite(0, 0);
            var sprite_laptop = this.add.sprite(0, 0);
            var sprite_wardrobe = this.add.sprite(0, 0);

            var sprite_month = this.add.sprite(0, 0);
            var sprite_dayH = this.add.sprite(0, 0);
            var sprite_dayL = this.add.sprite(0, 0);

            var sprite_armband = this.add.sprite(860, 415, 'imgArmbandScene6').setOrigin().setScale(0.5).setTint(0x0000ff).setAngle(-30).setInteractive();
            if (armbandPacked) {
                sprite_armband.visible = false;
                sprite_armband.disableInteractive();
            } else {
                sprite_armband.visible = true;
                sprite_armband.setInteractive();
            }

            var sprite_book = this.add.sprite(520, 715, 'imgBook').setOrigin(0).setScale(1.2);
            var sprite_clock = this.add.sprite(450, 745, 'imgClock').setOrigin(0);
            var sprite_tracker = this.add.sprite(325, 810, 'imgTracker').setOrigin(0);

            var sprite_sheet = this.add.sprite(1243, 416, 'imgSheet').setOrigin(0).setInteractive();
            if (paperOk) {
                sprite_sheet.visible = false;
                sprite_sheet.disableInteractive();
            }
            var sprite_printerClear = this.add.sprite(1520, 113, 'imgPrinterClear').setOrigin(0);
            sprite_printerClear.visible = false;
            var sprite_printerPrinted = this.add.sprite(1519, 328, 'imgPrinterPrinted').setOrigin(0).setInteractive();
            sprite_printerPrinted.visible = false;

            var sprite_listP1 = this.add.sprite(1364, 260, 'imgListPart1').setOrigin(0).setInteractive();
            if (listP1Ok) sprite_listP1.visible = false;

            var sprite_listP2 = this.add.sprite(450, 390, 'imgListPart2').setOrigin(0).setInteractive();
            if (listP2Ok) sprite_listP2.visible = false;

            if (paperOk && !winPrinter) {
                sprite_printerClear.visible = true;
                sprite_printerClear.setInteractive();
            }
            if (paperOk && winPrinter && !listOk) {
                sprite_printerPrinted.visible = true;
                sprite_printerPrinted.setInteractive();

                sprite_printerClear.visible = false;
                sprite_printerClear.disableInteractive();
            }
            if (listOk) {
                sprite_printerPrinted.visible = false;
                sprite_printerPrinted.disableInteractive();
            }

            var sprite_note3 = this.add.sprite(600, 420, 'imgNote3').setOrigin(0).setInteractive().setScale(1.75).setAngle(45);
            var sprite_note1 = this.add.sprite(250, 380, 'imgNote2').setOrigin(0).setInteractive();
            var sprite_note2 = this.add.sprite(420, 350, 'imgNote1').setOrigin(0).setInteractive();
            var sprite_note4 = this.add.sprite(300, 280, 'imgNote4').setOrigin(0).setInteractive().setScale(1.25);

            this.input.setDraggable(sprite_note1);
            this.input.setDraggable(sprite_note2);
            this.input.setDraggable(sprite_note3);
            this.input.setDraggable(sprite_note4);
            sprite_note1.setName('sNote1');
            sprite_note2.setName('sNote2');
            sprite_note3.setName('sNote3');
            sprite_note4.setName('sNote4');

            sprite_book.visible = false;
            sprite_clock.visible = false;
            sprite_tracker.visible = false;

            var sprite_book1 = this.add.sprite(0, 0, 'book3.0').setOrigin(0);
            var sprite_book2 = this.add.sprite(0, 0, 'book3.1').setOrigin(0);
            var sprite_book3 = this.add.sprite(0, 0, 'book3.2').setOrigin(0);
            sprite_book1.visible = false;
            sprite_book2.visible = false;
            sprite_book3.visible = false;

            var plgn_mainLeft = new Phaser.Geom.Polygon([830, 710, 1920, 670, 1920, 1080, 830, 1080]);
            var plgn_wardrobe = new Phaser.Geom.Polygon([1700, 0, 1920, 0, 1920, 860, 1780, 860, 1780, 350, 1700, 200]);
            var plgn_board = new Phaser.Geom.Polygon([250, 0, 1920, 0, 1920, 200, 250, 200]);
            var plgn_shelf = new Phaser.Geom.Polygon([100, 730, 830, 710, 830, 1080, 100, 1080]);
            var plgn_laptop = new Phaser.Geom.Polygon([860, 210, 1200, 130, 1360, 490, 1020, 600]);

            var plgn_month = new Phaser.Geom.Polygon([770, 285, 815, 295, 815, 350, 770, 340]);
            var plgn_dayH = new Phaser.Geom.Polygon([815, 295, 860, 305, 860, 360, 815, 350]);
            var plgn_dayL = new Phaser.Geom.Polygon([860, 305, 905, 315, 905, 370, 860, 360]);

            //var graphics = this.add.graphics();
            //graphics.fillStyle(0xffaa00);
            //graphics.fillPoints(plgn_wardrobe.points, true);


            //graphics.fillStyle(0xffaaff);
            //graphics.fillPoints(plgn_board.points, true);

            //graphics.fillStyle(0xaaaa00);
            //graphics.fillPoints(plgn_laptop.points, true);
            //graphics.fillStyle(0xaaaa00);
            //graphics.fillPoints(plgn_shelf.points, true);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);

            this.input.mouse.disableContextMenu();

            this.input.topOnly = true;

            sprite_mainLeft.setInteractive(plgn_mainLeft, Phaser.Geom.Polygon.Contains);
            sprite_wardrobe.setInteractive(plgn_wardrobe, Phaser.Geom.Polygon.Contains);
            sprite_board.setInteractive(plgn_board, Phaser.Geom.Polygon.Contains);
            sprite_shelf.setInteractive(plgn_shelf, Phaser.Geom.Polygon.Contains);
            sprite_laptop.setInteractive(plgn_laptop, Phaser.Geom.Polygon.Contains);

            sprite_month.setInteractive(plgn_month, Phaser.Geom.Polygon.Contains);
            sprite_dayH.setInteractive(plgn_dayH, Phaser.Geom.Polygon.Contains);
            sprite_dayL.setInteractive(plgn_dayL, Phaser.Geom.Polygon.Contains);

            sprite_mainLeft.on('pointerdown', function (pointer, gameObject) {
                if (shelfOpen) {
                    this.sound.play('mp3drawerClose');
                    shelfOpen = false;
                }
                this.scene.switch('MainSceneR');
            }, this);

            sprite_wardrobe.on('pointerdown', function (pointer, gameObject) {
                if (shelfOpen) {
                    this.sound.play('mp3drawerClose');
                    shelfOpen = false;
                }
                this.scene.switch('WardrobeScene');
            }, this);


            sprite_sheet.on('pointerdown', function (pointer, gameObject) {
                this.sound.play('mp3Sheet');
                paperOk = true;
                sprite_sheet.visible = false;
                sprite_sheet.disableInteractive();
                imgPrinterRed1.visible = false;

                sprite_printerClear.visible = true;
                sprite_printerClear.setInteractive();

                if (winPrinter) {
                    fxPrint = this.sound.add('mp3print');
                    fxPrint.play();
                    timedEvent = this.time.addEvent({
                        delay: 6000, callback: () => {

                            sprite_printerClear.visible = false;
                            sprite_printerClear.disableInteractive();

                            sprite_printerPrinted.visible = true;
                            sprite_printerPrinted.setInteractive();

                        }, callbackScope: this, repeat: 0, startAt: 0
                    });

                }
            }, this);

            sprite_printerPrinted.on('pointerdown', function (pointer, gameObject) {
                this.sound.play('mp3Sheet');
                listOk = true;

                sprite_printerPrinted.visible = false;

                timedEvent = this.time.addEvent({
                    delay: 500, callback: () => {

                        this.scene.start('BoardScene');

                    }, callbackScope: this, repeat: 0, startAt: 0
                });

            }, this);

            sprite_listP1.on('pointerdown', function (pointer, gameObject) {
                this.sound.play('mp3Sheet');
                listP1Ok = true;
                sprite_listP1.visible = false;
            }, this);

            sprite_listP2.on('pointerdown', function (pointer, gameObject) {
                this.sound.play('mp3Sheet');
                listP2Ok = true;
                sprite_listP2.visible = false;
            }, this);


            this.input.on('drag', function (pointer, gameObject, dragX, dragY) {



                if (dragX > 280 && dragX < 750) {
                    gameObject.x = dragX;
                }

                if (dragY > 300 && dragY < 480) {
                    gameObject.y = dragY;
                }
            });

            sprite_magazine.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('MagazineScene');
            }, this);

            sprite_board.on('pointerdown', function (pointer, gameObject) {
                if (shelfOpen) {
                    this.sound.play('mp3drawerClose');
                    shelfOpen = false;
                }
                this.scene.switch('BoardScene');
            }, this);

            sprite_shelf.on('pointerdown', function (pointer, gameObject) {

                if (winShelf) {
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
                        if (winBag) {
                            sprite_tracker.disableInteractive();
                            sprite_clock.disableInteractive();

                        }
                        sprite_book.visible = true;
                        sprite_book.setInteractive();
                        if (winBooks) {
                            sprite_book.disableInteractive();
                        }

                        imgSceneOpened.visible = true;

                    }

                    shelfOpen = !shelfOpen;
                } else {
                    this.scene.switch('ShelfScene');
                }

            }, this);

            sprite_laptop.on('pointerdown', function (pointer, gameObject) {
                if (!recordsOn) {
                    this.scene.start('LaptopScene');
                } else {
                    this.scene.start('Laptop2Scene');
                }
                if (shelfOpen) {
                    this.sound.play('mp3drawerClose');
                    shelfOpen = false;
                }
            }, this);

            sprite_book.on('pointerdown', function (pointer, gameObject) {
                sprite_book1.visible = true;
                sprite_book1.setInteractive();
            }, this);

            sprite_book1.on('pointerdown', function (pointer, gameObject) {
                sprite_book1.visible = false;
                sprite_book1.disableInteractive();

                sprite_book2.visible = true;
                sprite_book2.setInteractive();

                fxPage = this.sound.add('mp3page');
                fxPage.play();
            }, this);

            sprite_book2.on('pointerdown', function (pointer, gameObject) {
                sprite_book2.visible = false;
                sprite_book2.disableInteractive();

                sprite_book3.visible = true;
                sprite_book3.setInteractive();

                fxPage = this.sound.add('mp3page');
                fxPage.play();
            }, this);

            sprite_book3.on('pointerdown', function (pointer, gameObject) {
                sprite_book3.visible = false;
                sprite_book3.disableInteractive();

                fxPage = this.sound.add('mp3page');
                fxPage.play();

                book3Ok = true;

                if (book1Ok && book2Ok && book3Ok) {
                    winBooks = true;
                    fxPage = this.sound.add('mp3Mark1');
                    fxPage.play();
                    this.scene.start('BoardScene');
                }
            }, this);

            sprite_clock.on('pointerdown', function (pointer, gameObject) {

                sprite_clock.disableInteractive();
                sprite_clock.visible = false;
                clockPacked = true;
                armbandPacked = false;
                trackerPacked = false;
                sprite_tracker.visible = true;
                sprite_tracker.setInteractive();
                sprite_armband.visible = true;
                sprite_armband.setInteractive();
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
                sprite_armband.visible = true;
                sprite_armband.setInteractive();
                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_armband.on('pointerdown', function (pointer, gameObject) {

                sprite_armband.disableInteractive();
                sprite_armband.visible = false;
                trackerPacked = false;
                armbandPacked = true;
                clockPacked = false;
                if (shelfOpen) {
                    sprite_clock.visible = true;
                    sprite_clock.setInteractive();
                    sprite_tracker.visible = true;
                    sprite_tracker.setInteractive();
                }

                fxBag = this.sound.add('mp3bag');
                fxBag.play();
            }, this);

            sprite_month.on('pointerdown', function (pointer, gameObject) {
                this.sound.play('mp3Calendar');
                g_month++;
                if (g_month > 11) {
                    g_month = 0;
                }
                for (var i = 0; i < 12; i++) {
                    childMonth[i].visible = false;
                }
                childMonth[g_month].visible = true;

                if (g_month == 2 && g_day == 24 && winBooks && winBag && winMap && winTreadmill && winFile && winOpponents) {

                    this.sound.play('mp3yawn');

                }

            }, this);

            sprite_dayH.on('pointerdown', function (pointer, gameObject) {
                this.sound.play('mp3Calendar');
                g_day += 10;
                if (g_day >= 40) {
                    g_day = g_day - 40;
                }
                for (var i = 0; i < 4; i++) {
                    childDayH[i].visible = false;
                }
                childDayH[(g_day - g_day % 10) / 10].visible = true;
                if (g_month == 2 && g_day == 24 && winBooks && winBag && winMap && winTreadmill && winFile && winOpponents) {

                    this.sound.play('mp3yawn');

                }

            }, this);

            sprite_dayL.on('pointerdown', function (pointer, gameObject) {
                this.sound.play('mp3Calendar');
                if (g_day % 10 == 9) g_day -= 10;

                g_day++

                for (var i = 0; i < 10; i++) {
                    childDayL[i].visible = false;
                }
                childDayL[g_day % 10].visible = true;
                if (g_month == 2 && g_day == 24 && winBooks && winBag && winMap && winTreadmill && winFile && winOpponents) {

                    this.sound.play('mp3yawn');

                }
            }, this);

            sprite_hint.on('pointerdown', function (pointer, gameObject) {
                window.open(hintLink);
            }, this);

            sprite_hint.on('pointerover', function () {

                img_hint.visible = true;

            });

            sprite_hint.on('pointerout', function () {

                img_hint.visible = false;

            });
        }

        function createMagazineScene() {

            imgSceneClosed = this.add.image(0, 0, 'imgDeskClosedB').setOrigin(0);

            var groupMag = this.add.group();
            for (var i = 1; i <= 7; i++) {
                groupMag.create(0, 0, 'imgMag' + i).setOrigin(0);
            }
            var childMag = groupMag.getChildren();
            for (var i = 0; i < 7; i++) {
                childMag[i].visible = false;
            }
            childMag[pageMag].visible = true;

            var sprite_background = this.add.sprite(0, 0);
            var sprite_leftPage = this.add.sprite(0, 0);
            var sprite_rightPage = this.add.sprite(0, 0);

            var plgn_background = new Phaser.Geom.Polygon([0, 0, 1920, 0, 1920, 1080, 0, 1080]);
            var plgn_leftPage = new Phaser.Geom.Polygon([300, 170, 880, 120, 940, 1020, 300, 1060]);
            var plgn_rightPage = new Phaser.Geom.Polygon([920, 115, 1490, 90, 1590, 965, 970, 1025]);


            sprite_background.setInteractive(plgn_background, Phaser.Geom.Polygon.Contains);
            sprite_leftPage.setInteractive(plgn_leftPage, Phaser.Geom.Polygon.Contains);
            sprite_rightPage.setInteractive(plgn_rightPage, Phaser.Geom.Polygon.Contains);

            sprite_leftPage.on('pointerdown', function (pointer, gameObject) {

                if (pageMag) {
                    pageMag--;
                    this.sound.play('mp3page');
                    for (var i = 0; i < 7; i++) {
                        childMag[i].visible = false;
                    }
                    childMag[pageMag].visible = true;
                }

            }, this);

            sprite_rightPage.on('pointerdown', function (pointer, gameObject) {
                if (pageMag < 6) {
                    pageMag++;
                    this.sound.play('mp3page');
                    for (var i = 0; i < 7; i++) {
                        childMag[i].visible = false;
                    }
                    childMag[pageMag].visible = true;
                }
            }, this);

            sprite_background.on('pointerdown', function (pointer, gameObject) {
                this.scene.switch('DeskScene');
            }, this);

        }

        function createMarathonScene() {

            this.cameras.main.fadeIn(3000);
            var music = this.sound.add('mp3marathon');

            this.add.image(0, 0, 'imgM_bg').setOrigin(0);
            this.sound.play('mp3shoot');
            timedEvent = this.time.addEvent({ delay: 500, callback: () => { music.play();/*this.sound.play('mp3marathon');*/ }, callbackScope: this, repeat: 0, startAt: 0 });
            this.background_mounts = this.add.tileSprite(0, 430, 1980, 260, 'imgM_mounts').setOrigin(0);
            this.background_forest = this.add.tileSprite(0, 500, 1980, 220, 'imgM_forest').setOrigin(0);
            this.background_grass = this.add.tileSprite(0, 720, 1980, 30, 'imgM_grass0').setOrigin(0);
            this.background_road = this.add.tileSprite(0, 750, 1980, 330, 'imgM_road').setOrigin(0);

            //this.background_start = this.physics.add.sprite(1000, 750, 'imgM_start').setOrigin(0).setVelocityX(-100);


            timedEvent = this.time.addEvent({
                delay: 324000, callback: () => {
                    this.background_finish = this.physics.add.sprite(2000, 750, 'imgM_finish').setOrigin(0).setVelocityX(-120);

                }, callbackScope: this, repeat: 0, startAt: 0
            });

            timedEvent = this.time.addEvent({
                delay: 328500, callback: () => {
                    // music.stop();
                    this.cameras.main.fadeOut(3000);
                    // this.sound.stop('mp3marathon');
                }, callbackScope: this, repeat: 0, startAt: 0
            });

            this.background_start = this.physics.add.sprite(1000, 750, 'imgM_start').setOrigin(0).setVelocityX(-100);
            timedEvent = this.time.addEvent({
                delay: 330000, callback: () => {
                    this.scene.start('FinalScene');
                    music.stop();

                    // this.cameras.main.fadeOut(3000);
                    // this.sound.stop('mp3marathon');
                }, callbackScope: this, repeat: 0, startAt: 0
            });



            this.buildingsGroup = this.add.group();
            this.skiesGroup = this.add.group();
            this.frontGroup = this.add.group();

            platform = this.physics.add.sprite(-300, 372, "imgM_b1").setOrigin(0).setVelocityX(-100);
            platform.displayWidth = 150;
            this.nextBuildDistance = 300;
            this.nextSkiesDistance = 0;
            this.nextFrontDistance = 300;
            this.buildingsGroup.add(platform);

            text = this.add.text(10, 10, '', { fill: '#aaffff' }).setDepth(1);


            this.anims.create({
                key: 'runner0',
                frames: [
                    { key: 'imgM_R0_1' },
                    { key: 'imgM_R0_2' },
                    { key: 'imgM_R0_3' },
                    { key: 'imgM_R0_4' },
                    { key: 'imgM_R0_5' },
                    { key: 'imgM_R0_6' }
                ],
                frameRate: 5,
                repeat: -1
            });

            this.anims.create({
                key: 'runner1',
                frames: [
                    { key: 'imgM_R1_1' },
                    { key: 'imgM_R1_2' },
                    { key: 'imgM_R1_3' },
                    { key: 'imgM_R1_4' },
                    { key: 'imgM_R1_5' },
                    { key: 'imgM_R1_6' }
                ],
                frameRate: 5,
                repeat: -1
            });

            this.anims.create({
                key: 'runner2',
                frames: [
                    { key: 'imgM_R2_1' },
                    { key: 'imgM_R2_2' },
                    { key: 'imgM_R2_3' },
                    { key: 'imgM_R2_4' },
                    { key: 'imgM_R2_5' },
                    { key: 'imgM_R2_6' }
                ],
                frameRate: 5,
                repeat: -1
            });

            this.anims.create({
                key: 'runner3',
                frames: [
                    { key: 'imgM_R3_1' },
                    { key: 'imgM_R3_2' },
                    { key: 'imgM_R3_3' },
                    { key: 'imgM_R3_4' },
                    { key: 'imgM_R3_5' },
                    { key: 'imgM_R3_6' }
                ],
                frameRate: 5,
                repeat: -1
            });

            this.anims.create({
                key: 'runner4',
                frames: [
                    { key: 'imgM_R4_1' },
                    { key: 'imgM_R4_2' },
                    { key: 'imgM_R4_3' },
                    { key: 'imgM_R4_4' },
                    { key: 'imgM_R4_5' },
                    { key: 'imgM_R4_6' }
                ],
                frameRate: 5,
                repeat: -1
            });

            this.anims.create({
                key: 'runner5',
                frames: [
                    { key: 'imgM_R5_1' },
                    { key: 'imgM_R5_2' },
                    { key: 'imgM_R5_3' },
                    { key: 'imgM_R5_4' },
                    { key: 'imgM_R5_5' },
                    { key: 'imgM_R5_6' }
                ],
                frameRate: 5,
                repeat: -1
            });

            this.anims.create({
                key: 'runner6',
                frames: [
                    { key: 'imgM_R6_1' },
                    { key: 'imgM_R6_2' },
                    { key: 'imgM_R6_3' },
                    { key: 'imgM_R6_4' },
                    { key: 'imgM_R6_5' },
                    { key: 'imgM_R6_6' }
                ],
                frameRate: 5,
                repeat: -1
            });

            this.anims.create({
                key: 'runner7',
                frames: [
                    { key: 'imgM_R7_1' },
                    { key: 'imgM_R7_2' },
                    { key: 'imgM_R7_3' },
                    { key: 'imgM_R7_4' },
                    { key: 'imgM_R7_5' },
                    { key: 'imgM_R7_6' }
                ],
                frameRate: 5,
                repeat: -1
            });

            this.anims.create({
                key: 'runner8',
                frames: [
                    { key: 'imgM_R8_1' },
                    { key: 'imgM_R8_2' },
                    { key: 'imgM_R8_3' },
                    { key: 'imgM_R8_4' },
                    { key: 'imgM_R8_5' },
                    { key: 'imgM_R8_6' }
                ],
                frameRate: 5,
                repeat: -1
            });

            this.runner0 = this.physics.add.sprite(800, 820, 'imgM_R1_1').setScale(0.9).setDepth(820).play('runner0');

            this.runnersGroup = this.add.group();
            for (i = 0; i < 200; i++) {
                runnerSkin = Phaser.Math.Between(1, 8);
                runnerYpos = Phaser.Math.Between(720, 870);
                velocityRunners[i] = Phaser.Math.Between(-450, -80);
                runner = this.physics.add.sprite(Phaser.Math.Between(200, 700), runnerYpos, 'imgM_R' + runnerSkin + '_1').setScale(1 - (870 - runnerYpos) / 500).setDepth(runnerYpos).play('runner' + runnerSkin).setVelocityX(velocity - velocityRunners[i]);
                this.runnersGroup.add(runner);
            }






            timedEvent = this.time.addEvent({ delay: 500, callback: () => { if (velocity <= -100) velocity += 10; }, callbackScope: this, repeat: -1, startAt: 0 });
            this.input.on('pointerdown', function (pointer) {

                velocity -= 10;
                if (velocity <= -500) velocity = -500;

            }, this);

            this.input.mouse.disableContextMenu();

            // this.input.topOnly = true;
        }




        function updateMainScene0() {
            //var pointer = this.input.activePointer;
            //text.setText([
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateMainSceneR() {
            //var pointer = this.input.activePointer;
            //text.setText([
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateWardrobeScene() {
            //var pointer = this.input.activePointer;
            //text.setText([
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateSportsbagScene() {
            //var pointer = this.input.activePointer;
            //text.setText([
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateTreadmillScene() {

            //var pointer = this.input.activePointer;
            //text.setText([
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown(),
            //    'tap: ' + tap
            //]);


        }

        function updateBedScene() {
            //var pointer = this.input.activePointer;
            //text.setText([
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateMapScene() {


            //var pointer = this.input.activePointer;
            //text.setText([
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'fill1: ' + setA2,
            //    'fill2: ' + setB4,
            //    'fill3: ' + setC1,
            //    'fill4: ' + setD2,

            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateBoardScene() {
            //var pointer = this.input.activePointer;
            //text.setText([
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateShelfScene() {
            //var pointer = this.input.activePointer;
            //text.setText([
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateLaptopScene() {

            //var pointer = this.input.activePointer;
            //text.setText([
            //    'tap: ' + tap,
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateLaptop2Scene() {
            //var pointer = this.input.activePointer;
            //text.setText([
            //    'tap: ' + tap,
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);

            printerCount.setText([
                printerPass
            ]);

            fileL1.setText([
                alphabet[fileL1Pass]
            ]);
            fileL2.setText([
                alphabet[fileL2Pass]
            ]);
            fileL3.setText([
                alphabet[fileL3Pass]
            ]);
        }

        function updateLaptop3Scene() {
            //var pointer = this.input.activePointer;
            //text.setText([
            //    'tap: ' + tap,
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateDeskScene() {
            //var pointer = this.input.activePointer;
            //text.setText([
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateMagazineScene() {
            //var pointer = this.input.activePointer;
            //text.setText([
            //    'x: ' + pointer.worldX,
            //    'y: ' + pointer.worldY,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);
        }

        function updateMarathonScene() {
            this.background_mounts.tilePositionX += velocity / (-6000);
            this.background_forest.tilePositionX += velocity / (-600);
            this.background_grass.tilePositionX += velocity / (-300);
            this.background_road.tilePositionX += velocity / (-50);



            //if (this.background_start.x < - 1000) {
            //    this.background_start.destroy();
            //}

            var chldB = this.buildingsGroup.getChildren();
            for (i = 0; i < this.buildingsGroup.getLength(); i++) {
                chldB[i].setVelocityX(velocity);
            }
            // recycling platforms

            this.buildingsGroup.getChildren().forEach(function (platform) {

                if (platform.x < - platform.displayWidth) {
                    this.buildingsGroup.killAndHide(platform);
                    this.buildingsGroup.remove(platform);
                }
            }, this);

            var minDistance = 1920;
            var platformDistance = 1920;
            if (this.buildingsGroup.getLength()) {
                x = chldB[this.buildingsGroup.getLength() - 1].x;
                w = chldB[this.buildingsGroup.getLength() - 1].displayWidth;
                platformDistance = 2120 - x - w;
            }

            if (platformDistance) {
                minDistance = Math.min(minDistance, platformDistance);
            }


            // adding new builds
            if (minDistance > this.nextBuildDistance) {
                var nextBuilding = Phaser.Math.Between(1, 8)
                //var nextPlatformWidth = Phaser.Math.Between(gameOptions.platformSizeRange[0], gameOptions.platformSizeRange[1]);
                //this.addPlatform(nextPlatformWidth, game.config.width + nextPlatformWidth / 2);
                if (!marathonRestarted) {
                    marathonRestarted = true;
                    platform = this.physics.add.sprite(-2520, 375, "imgM_b" + nextBuilding).setOrigin(0).setScale(1.5);
                    //platform.setImmovable(true);
                    platform.setVelocityX(velocity);
                    this.buildingsGroup.add(platform);

                    platform.displayWidth = buildingsWidth[nextBuilding - 1];
                    this.nextBuildDistance = Phaser.Math.Between(0, 50);
                } else {

                    platform = this.physics.add.sprite(2120 + buildingsWidth[nextBuilding - 1] / 4, 375, "imgM_b" + nextBuilding).setOrigin(0).setScale(1.5);

                    platform.setImmovable(true);
                    platform.setVelocityX(velocity);
                    this.buildingsGroup.add(platform);
                    platform.displayWidth = buildingsWidth[nextBuilding - 1];
                    this.nextBuildDistance = Phaser.Math.Between(10, 100);
                }
            }


            //skies
            let minDistanceSkies = 1920;
            this.skiesGroup.getChildren().forEach(function (platform) {
                let skiesDistance = 1920 - platform.x - 300;
                minDistanceSkies = Math.min(minDistanceSkies, skiesDistance);
                if (platform.x < -2000) {
                    this.skiesGroup.killAndHide(platform);
                    this.skiesGroup.remove(platform);
                }
            }, this);

            // adding new skies
            if (minDistanceSkies > this.nextSkiesDistance) {
                platform = this.physics.add.sprite(1920 + 600, 0, 'imgM_sky' + Phaser.Math.Between(1, 2)).setOrigin(0);
                // platform.setImmovable(true);
                platform.setVelocityX(-50);
                this.skiesGroup.add(platform);
                this.nextSkiesDistance = Phaser.Math.Between(0, 600);
            }

            var chld = this.skiesGroup.getChildren();
            for (i = 0; i < this.skiesGroup.getLength(); i++) {
                chld[i].setScale(1 + (1920 - chld[i].x) / 1750)
            }

            //front
            let minDistanceFront = 1920;
            this.frontGroup.getChildren().forEach(function (platform) {
                let frontDistance = 1920 - platform.x - 200;
                minDistanceFront = Math.min(minDistanceFront, frontDistance);
                if (platform.x < -500) {
                    this.frontGroup.killAndHide(platform);
                    this.frontGroup.remove(platform);
                }
            }, this);

            // adding new fronts
            if (minDistanceFront > this.nextFrontDistance) {
                platform = this.physics.add.sprite(1920 + 350, 1000, 'imgM_front' + Phaser.Math.Between(1, 2)).setScale(0.9).setOrigin(0).setDepth(1000);
                // platform.setImmovable(true);
                platform.setVelocityX(velocity * 1.5);
                this.frontGroup.add(platform);
                this.nextFrontDistance = Phaser.Math.Between(0, 950);
            }

            var chldF = this.frontGroup.getChildren();
            for (i = 0; i < this.frontGroup.getLength(); i++) {
                chldF[i].setVelocityX(velocity * 1.5);
            }

            this.runner0.anims.msPerFrame = 200 + velocity / 5;
            if (this.background_start) {
                this.background_start.setVelocityX(velocity - 25);
            }
            if (this.background_finish) {
                this.background_finish.setVelocityX(velocity - 25);
            }
            var chldR = this.runnersGroup.getChildren();
            for (i = 0; i < this.runnersGroup.getLength(); i++) {
                chldR[i].anims.msPerFrame = 200 + velocityRunners[i] / 5;
                chldR[i].setVelocityX(velocity - velocityRunners[i])
            }








            //var pointer = this.input.activePointer;
            //text.setText([
            //    //'x: ' + this.runner1.anims.msPerFrame,
            //    'y: ' + this.runner1v,
            //    'n: ' + velocity,
            //    'isDown: ' + pointer.isDown,
            //    'rightButtonDown: ' + pointer.rightButtonDown()
            //]);


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
