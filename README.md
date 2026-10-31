local _ = {
  ["x"] = 10,
  ["y"] = 20,
  ["z"] = function(a, b)
    local c = a + b
    return c * 2
  end
}

local function q()
  local s = "lua"
  local r = 0
  for i = 1, 5 do
    r = r + i
  end
  return s, r, _["z"](3, 4)
end

local a, b, c = q()
print(a, b, c)
if c > 10 then
  print("wow")
else
  print("meh")
end
