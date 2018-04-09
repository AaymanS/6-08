-----------------------------------------------------------------------------------------
-- Created by: Aayman Shameem
-- Created on: Apr 09, 2018
--
-- This code will multiply two integers together
-----------------------------------------------------------------------------------------
-- first input
local titleText1 = display.newText( "First number:", display.contentCenterX - 570, display.contentCenterY - 570, native.systemFont, 177 )

-- second input
local titleText2 = display.newText( "Second number:", display.contentCenterX - 570, display.contentCenterY - 177, native.systemFont, 177 )

-- the place for first input
local firstInput = native.newTextField( display.contentCenterX + 520, display.contentCenterY - 570, 720, 277 )
-- the place for second input
local secondInput = native.newTextField( display.contentCenterX + 520, display.contentCenterY - 177, 720, 277 )

-- the answer of the question
local answerText = display.newText( ".....", display.contentCenterX, display.contentCenterY + 520, native.systemFont, 177 )

-- the multiplication button
local timesButton = display.newImageRect( "./assets/sprites/enterButton.png", 675, 277 )
timesButton.x = display.contentCenterX 
timesButton.y = display.contentCenterY + 177
timesButton.id = "the multiplying button"

local function theTimesButton ( event )

	local looping 
	local test = 1
	local answer = 0
	local number1 = tonumber( firstInput.text )
	local number2 = tonumber( secondInput.text )
		
	for looping = test,number1 do
		answer = answer + number2
		
	end
	answerText.text = "" .. answer .. ""
end

timesButton:addEventListener( "touch", theTimesButton )
