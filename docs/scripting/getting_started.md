# Getting started

To get credentials for the Moona repository ping Maris.

1. Clone the [main repository](https://gitlab.com/chtammik/MoonaAudio.git) and copy the contents to your Unity project (preferably `Assets/Plugins/Moona/`)
2. From the top menu select `Moona/Editor/Setup/Initialize` to generate a fresh `MConfig` file and a basic folder structure

It is possible to host Moona as a **git submodule** or **git subproject** to tie the versioned Moona code into your project.

## Project layout

The Moona plugin folder structure is as follows:

	Assets/Plugins/Moona/
		Modules/              # The various code modules of Moona	   # 
			Assets/	   		  # TODO: describe modules
			Components/	   	  # 
			Core/	   		  # 
			Debug/	    	  # 
			Editor/	   		  # 
			Extensions/		  # 
			Mixer/			  # 
			Music/			  # 
			Reverb/			  # 
			RTPC/	   		  # 
			Spatialization/	  # 
			VoiceManagement/  # 		

The Moona project folder structure is as follows:

	Assets/Moona/
		MoonaConfig.asset     # The configuration file for documentation
		MDebugLog.asset       # An editor asset for holding a timeline of played MObjects
		Data/                 # This folder contains all MObjects
		MoonaExtension/       # Project specific extensions to Moona (optional)

## Initializing Moona in game

The central system initialization is being handled by the `MSetup` script. A reference to the `MConfig` asset we just created is required. The default location for this asset `Assets/Plugins/Moona/MConfig.asset`.

```
    // passing in an MConfig.asset to initialize Moona
    MSetup.Initialize(this.Config);
```

It is also possible to attach the MSetup scrip to your gams' camera or game controller prefab. This allows it to initialize in any scene easily. Remeber to place a reference to the MConfig file.

## Documentation

You are currently looking at it! It is beinge served on [github pages](https://fuzzblob.github.io/moonadocs/).

If you want to read it locally you have the option of either to either run [MkDocs](https://www.mkdocs.org/) to present it as a local website or to read the Markdown files on their own (a markdown compatible viewer would be reccommended).

The pubically available [documentation repo](https://github.com/fuzzblob/moonadocs) also contains a Doxygen configuration which can be used to generate a full scripting API documentation (with all methods and fields as well call graphs etc). A built version (html or PDF) available upon request.

## Testing Repository

Another useful resource might be the [Moona_Testing](https://gitlab.com/chtammik/Moona_Testing.git) repository (same credentials as main repository). It is used for experimentation and Unit-/Integration testing.