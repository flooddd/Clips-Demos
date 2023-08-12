# DemoScraper
A python script that searches through over 1,800 csgo demos from various youtube channels to find demos specific to what you searched for.

TYPE "!help" TO GET HELP!
IF YOU HAVE QUESTIONS DM ME ON DISCORD - flowde

Each keyword you add (case INsensitive: ak == AK) MUST BE IN THE DEMO name to be output. For example: AK 3K will return: "Flood 3k ak47 cache" but NOT "Flood 3k cache"

ADVANCED SEARCHING (LOGIC):
To add a keyword that must NOT be in the search, ie only return demos that are NOT on mirage, use the "not" or "!" keywords.
EXAMPLE: "ak47 not mirage"
EXAMPLE: "awp not overpass noscope" - NOTE: The "not" ONLY NEGATES THE "overpass", or first keyword to the right! This means that "noscope" will still be included in the search

To add two keywords that can either be in the search, use the "or" or "||" keywords.
EXAMPLE: "usp cache or mirage" will return demos using a usp on either the maps cache or mirage
EXAMPLE: "overpass ak or awp" will return demos on overpass using either the ak or the awp

AUTO KEYWORDS:
Use this function when using consistent keywords, ie every search will include mirage, and you don't want to keep typing that word in the query.
EXAMPLE: "!addkw overpass" This will add overpass to every single following query, until cleared. If the next query is "ak47", demos on overpass that use the ak will be returned
EXAMPLE: "!addkw mirage or vertigo" LOGIC ALSO WORKS WITH AUTO KEYWORDS!
TO CLEAR AUTO KEYWORDS, type "!clearkw"

ROGUE KEYWORDS:
IF YOUR SEARCH RETURNS 0 DEMOS, THE SCRIPT WILL DETECT KEYWORDS THAT WERE NOT FOUND IN ANY DEMO AT ALL!
This is usually due to a mispelling. If the rogue keyword is close enough to a commonly used keyword, it may suggest a correct spelling
IF THERE ARE NO DEMOS FOUND AND STILL NO ROGUE KEYWORDS, YOUR SEARCH HAD AN INNER CONTRADICTION
EXAMPLE: "overpass mirage" will return 0 demos, because demos cannot take place on both maps at once. No rogue keywords will be found, since each word was detected in at least one demo, but not both
TIP: To avoid this, use the "or" logic to use contradicting keywords: "overpass or mirage"
