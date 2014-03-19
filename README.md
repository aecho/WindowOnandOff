WindowOnandOff
==============
local myBuilding = {display.newRect( 200, 500, 300, 500)} 


--myBuilding.x = myBuilding.x + ( bldgWidth * 0.25 )
--myBuildingShadow.y = myBuilding.y * 1.0125
--myBuildingShadow.fill = paintWarmGrey


local function pickColor() 

	local index=math.random(0,1) 
	local onColor=0.525,0.6125,0.575,1  
	local offColor=0,0,0,1 
        local myColor=nil 
	if index==0 then 
            myColor=onColor 
	elseif index==1 then 
            myColor=offColor 
	end

        return myColor 
end

local function listener( event ) 

	for i = 1, 6 do  
		for j = 1, 4 do 
		    local mywindow = display.newRect(75+j*50, 300+i*60, 20, 20) 
		    local windowColor=pickColor()  
		    mywindow:setFillColor(windowColor)	
	end
end
end

local levelTime = 60 
