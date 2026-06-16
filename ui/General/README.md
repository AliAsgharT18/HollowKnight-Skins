# HollowKnightSkin
this is a simple Skin for my Hollow Knight Project

use this sample code to apply the skin in your project
(first putt all the files in asset/ui in your gradle project)

skin = new Skin();
        com.badlogic.gdx.graphics.g2d.TextureAtlas atlas =
            new com.badlogic.gdx.graphics.g2d.TextureAtlas(Gdx.files.internal("ui/HollowSkin.atlas"));
        skin.addRegions(atlas);
        FreeTypeFontGenerator generator = new FreeTypeFontGenerator(Gdx.files.internal("ui/TrajanPro-Regular.ttf"));
        FreeTypeFontGenerator.FreeTypeFontParameter param = new FreeTypeFontGenerator.FreeTypeFontParameter();
        param.size = 24;
        BitmapFont font = generator.generateFont(param);
        generator.dispose(); // Free generator memory
        skin.add("Hollowfont", font, BitmapFont.class);
        skin.load(Gdx.files.internal("ui/HollowSkin.json"));
