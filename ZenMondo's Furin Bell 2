integer isOn;

float minTime = 0.3;
float maxTime = 5.0;

float minVol = 0.2;
float maxVol = 1.0;

float randBetween(float min, float max)
{
    return llFrand(max - min) + min;
}


default
{
    state_entry()
    {
        
    }

    touch_start(integer total_number)
    {
        if(isOn)
        {
            llSetTimerEvent(0);
            isOn = FALSE;
            llWhisper(0, "Bell off");
        }
        
        else
        {
            llSetTimerEvent(randBetween(minTime, maxTime));
            isOn = TRUE;
            llWhisper(0, "Bell on");
        }
    }
    
    timer()
    {
        llPlaySound(llGetInventoryName(INVENTORY_SOUND, 0), randBetween(minVol, maxVol));        
        llSetTimerEvent(randBetween(minTime, maxTime));
    }
}
