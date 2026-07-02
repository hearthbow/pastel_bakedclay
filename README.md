# pastel_bakedclay
Fork of bakedclay mod by TenPlus1 on Minetest/Luanti to create pastel variations.

Supports circular saw from moreblocks and mymillwork. Could not register it in facade mod with the API, if you want to register it in facade you can paste:

if minetest.get_modpath( "pastel_bakedclay") then

local pc = {
-- name, description
  {"pink", "Pastel Pink"},
	{"lightpink", "Pastel Light Pink"},
	{"orange", "Pastel Orange"},
	{"purple", "Pastel Purple"},
	{"yellow", "Pastel Yellow"},
	{"blue", "Pastel Blue"},
	{"olivegreen", "Pastel Olive Green"},
	{"mintgreen", "Pastel Mint Green"},
	{"cyan", "Pastel Cyan"},
	{"red", "Pastel Red"},
	
}
for _, row in ipairs(pc) do
      facade.register_facade_nodes("pastel_bakedclay", row[1] , "pastel_bakedclay:" .. row[1], row[2] .. " Baked Clay")
   end
end

Into your facade mod in materials.lua
