stick this in your variables s_player_robbank = -1;
Then shove this bad boy in your fn_selfActions.sqf

 _bankrobbery = cursorTarget isKindOf "Notebook";
    if ((speed player <= 1) && _bankrobbery && (player distance cursorTarget < 5)) then {
        if (s_player_bankrob < 0) then {
            s_player_bankrob = player addAction ["Rob the bank","yourfilepath\robbank.sqf",cursorTarget, 0, false, true, "",""];
        };
    } else {
       
        player removeAction s_player_bankrob;
		s_player_bankrob = -1;
    };
	
	then sick this at the bottom with the rest of your custom shit 
	  player removeAction s_player_bankrob;
		s_player_bankrob = -1;
		
	open your description.ext like a flower in bloom
then add this shit take the whole line if your using radion for WAI

class CfgSounds
{
    sounds[] =
    {
        Radio_Message_Sound
    };
    class Radio_Message_Sound
    {
        name = "Radio_Message_Sound";
        sound[] = {dayz_code\external\radio\radio.ogg,0.4,1};
        titles[] = {};
    };
    sounds1[] =
    {
    siren
    };
    class siren
    {
    name="siren";
    sound[]={dayz_code\external\rob\siren.ogg,0.9,1};
    titles[] = {};
    };
};  
"This makes a lovely noise when robbing...... for fun i put it there for fun"
