# LANC-SEND---RECEIVE---ARDUINO
A simple code with no libraries to Send  AND receive LANC command in the same time ! 

LOT OF THANKS TO KOCH Martin, ROCHOLL Ariel and... GPT Chat !

2 days on this freaking code ! Just some error like the forgotten nCommandTimes = 0; ligne 221 to reset the Command Time ! 

I Will add in few day all the LANC code from Martin and Me  !

Example : (From http://www.boehmel.de/lanc#byte2)

const boolean LANC_CAM_CONTROL::REC[16] = {LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, HIGH, HIGH};
const boolean LANC_CAM_CONTROL::ZOOM_IN[8][16] = {
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, LOW, LOW, LOW, LOW, LOW}, // 0
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, LOW}, // 1
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, LOW, LOW}, // 2
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, HIGH, LOW}, // 3
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, LOW, LOW, LOW}, // 4
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, LOW, HIGH, LOW}, // 5
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, HIGH, LOW, LOW}, // 6
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, HIGH, HIGH, LOW}  // 7
};
const boolean LANC_CAM_CONTROL::ZOOM_OUT[8][16] = {
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, LOW, LOW, LOW, LOW}, // 0
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, LOW, LOW, HIGH, LOW}, // 1
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, LOW, HIGH, LOW, LOW}, // 2
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, LOW, HIGH, HIGH, LOW}, // 3
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW}, // 4
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, HIGH, LOW, HIGH, LOW}, // 5
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, HIGH, HIGH, LOW, LOW}, // 6
    {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, LOW, HIGH, HIGH, HIGH, HIGH, LOW}  // 7
};
const boolean LANC_CAM_CONTROL::FOCUS_NEAR[16] = {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, HIGH, LOW, LOW, LOW, HIGH, HIGH, HIGH};
const boolean LANC_CAM_CONTROL::FOCUS_FAR[16] = {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, HIGH, LOW, LOW, LOW, HIGH, LOW, HIGH};
const boolean LANC_CAM_CONTROL::FOCUS_AUTO[16] = {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, LOW, HIGH, LOW, LOW, LOW, LOW, LOW, HIGH};
const boolean LANC_CAM_CONTROL::POWER_OFF[16] = {LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, LOW, HIGH, HIGH, LOW, HIGH, HIGH, HIGH, LOW};
const boolean LANC_CAM_CONTROL::POWER_ON[16] = {LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, LOW, HIGH, HIGH, LOW, HIGH, LOW, LOW, LOW};
const boolean LANC_CAM_CONTROL::POWER_RESTART[16] = {LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, LOW, LOW, HIGH, LOW, HIGH, LOW, HIGH, LOW};
const boolean LANC_CAM_CONTROL::POWER_SLEEP[16] = {LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, LOW, HIGH, LOW, HIGH, LOW, HIGH, LOW, LOW};
const boolean LANC_CAM_CONTROL::MENU[16] = {LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, HIGH, LOW, LOW, HIGH, HIGH, LOW, HIGH, LOW};
const boolean LANC_CAM_CONTROL::UP[16] = {LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, HIGH, LOW, LOW, LOW, LOW, HIGH, LOW, LOW};
const boolean LANC_CAM_CONTROL::DOWN[16] = {LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, HIGH, LOW, LOW, LOW, LOW, HIGH, HIGH, LOW};
const boolean LANC_CAM_CONTROL::LEFT[16] = {LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, HIGH, LOW, LOW};
const boolean LANC_CAM_CONTROL::RIGHT[16] = {LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, LOW, HIGH, LOW};
const boolean LANC_CAM_CONTROL::EXECUTE[16] = {LOW, LOW, LOW, HIGH, HIGH, LOW, LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW, HIGH, LOW};
