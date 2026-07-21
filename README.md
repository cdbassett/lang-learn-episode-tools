# lang-learn-episode-tools
Python scripts to help process video files in episodic format with the end goal being language learning. It achieves this via mass creation of subtitle files for entire seasons that include the native language, the user's language, and optionally dictonary lookups from the native language to the user's languge. The initial purpose was for an English speaker learning Japanese (primarily anime) but most of the scripts could be used for any language.

# Simple listing of scripts:

## Bulk operations (over mutliple shows)
	RenameAnimeDirs
		to use better overall folder names while preserving original name in a file
	ReportMultiAudioStreamFolders
		Report folders with video files with multiple audio streams
	ScanKitsuNekko
		scan KitsuNekko web page for matches in English and Japanese sub file
    
## Video file operations
	ExtractSubs
		if need e.g. English subtitle files that are embdedded in video files
	ReduceStreams
		remove English audio from video files
	VerifyReducedStreamVideos
		Check video files that have been reduced by ReduceStreams.py to see if they are still valid
	CopyStreams
		Copy video files to new containers using ffmpeg.
	SetMKVLangTags
		Fix incorrect language tags in MKV streams
	SetMKVTitleTags
		Fix incorrect title tags in MKV streams
	AvgVidSize
		list avg size of video files per main anime folder

## Subtitle file operations
	RenumberEpisodes
		rename subtitle files to match video files by regex matching
	RenSubs
		to make Japanese subtitle filenames the same as the English versions
	AnalyzeSubs
		Analyze subtitle files and report total duration, lines, number of files present for every style
	PlotSubs
		Create a graphical representation of the English and Japanese subs side by side
	AlterStyles
		Alter subtitle styles in subtitle files
	RemoveChineseSubStyles
		if chinese subs are also in Japanese subtitle files, remove them
	ChopSubLines
		Remove all but first line of multiline subs (sometimes Japanese subs have Japanese as first line, then Chinese on following lines)
	CleanJACC
		Clean Japanese CC artifacts (sound effects,music, etc.)
	ConvertSubsToSRT
		Convert subtitle files to srt
	RecodeSubFiles
		Convert subtitle files from one encoding to another.
	RemoveSubEffects
		Remove subtitle events with certain effects
	RemoveSubStyles
		Remove subtitle styles
	AdjustJaSubsFromEn
		sync timestamps in Japanese subtitle files to match English subtitle files
	AdjustEnSubsFromJa
		Adjust timings of English subs from reference Japanese subs (not used nearly as often as AdjustJaSubsFromEn)
	AdjustJaSubsFromVid
		Adjust timings of Japanese subs from video files (experiemental)
	GenerateJESubs
		create new dictionary entry subtitle files (both long .je and short .jw) from Japanese subtitle files
	MergeJaEnSubs
		Merge Japanese and English subtitle files into one, with Japanese on top. (ja-en)
	MergeJaJeSubs
		Merge Japanese subtitle files and long dictionary subtitle files into new subtitle files
	MergeJwEnSubs
		Merge Japanese and short Dictionary and English subtitle files into new subtitle files
	MovePreMerged
		After processing is done, move non-final subtitle files to a folder for cleaner use
	7zsubs
		Create 7z files of subtitles for backup and adding to Kitsunekko
	TrimSubs
		Remove sub events that fall outside of specified time ranges

## RenVidInfo
	rename metadata files to match new video name. assuming deleted old video, and want previous metadata filenames to match new file
