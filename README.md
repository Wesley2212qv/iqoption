
instrument{name="INSTAGRAM:EDWUARD TRADER",icon='https://lh3.googleusercontent.com/ogw/ADea4I65OapvF7ZOUMZc_3J4Yx__qVmvJD_jgzr4p8MZNks=s32-c-mo',overlay=true}

local function a()local 
b=make_series()local c=high[2]

if not get_value(c)then 
return b end;
local d=high<=c and high[1]<=c and high[3]<=c and high[4]<=c;
b:set(iff(d,c,b[1]))return b end;
local function e()local b=make_series()local c=low[2]if not get_value(c)then return b end;
local d=low>=c and low[1]>=c and low[3]>=c and low[4]>=c;
b:set(iff(d,c,b[1]))return b end;
input_group{"Color",color=input{default="white",type=input.color},width=input{default=1,type=input.line_width}}h=a()l=e()hline(h,"High",color,high_width)hline(l,"Low",color,width)hline(highest(10)[1],"HH10",color,1)hline(lowest(10)[1],"LL10",color,1)hline(highest(30)[1],"HH30",color,1)hline(lowest(30)[1],"LL30",color,1)hline(highest(60)[1],"HH60",color,1)hline(lowest(60)[1],"LL60",color,1)hline(highest(100)[1],"HH100",color,1)hline(lowest(100)[1],"LL100",color,1)hline(highest(150)[1],"HH150",color,1)hline(lowest(150)[1],"LL150",color,1)hline(highest(200)[1],"HH200",color,1)hline(lowest(200)[1],"LL200",color,1)

instrument { name = "INSTAGRAM:EDWUARD DIAZ", icon="indicators:ADX", overlay = true }
method_id = input (1, "Type", input.string_selection, { "INSTAGRAM:EDWUARD DIAZ" })


instrument {
    name = 'INSTAGRAM:EDWUARD DIAZ',
    short_name = 'INSTAGRAM:EDWUARD DIAZ',
  icon = 'indicators:BB',
    overlay = true
}

MaFast_period = input(1,"Ma Fast period",input.integer,1,1000,1)
MaValue = input(5,"Ma Value", input.string_selection,inputs.titles)

MaSlow_period = input(34,"Ma Slow period",input.integer,1,1000,1)

Signal_period = input(5,"Signal period",input.integer,1,1000,1)

input_group {
    "Compra",
    colorBuy = input { default = "green", type = input.color }, 
    visibleBuy = input { default = true, type = input.plot_visibility }
}

input_group {
    "Venda",
    colorSell = input { default = "red", type = input.color },
    visibleSell = input { default = true, type = input.plot_visibility }
}

local titleValue = inputs[MaValue]

-- mdia mvel linear rpida
smaFast = sma(titleValue, MaFast_period)

-- mdia mvel linear devagar
smaSlow = sma(titleValue, MaSlow_period)

-- calculo diferencial - serie
buffer1 = smaFast - smaSlow 

-- clculo da mdia mvel ponderada - serie
buffer2 = wma(buffer1, Signal_period)

buyCondition = conditional(buffer1 > buffer2 and buffer1[1] < buffer2[1] and not (buffer1 < buffer2 and buffer1[1] > buffer2[1]))
buyCondition = conditional(buffer1 > buffer2 and buffer1[1] < buffer2[1])

sellCondition = conditional(buffer1 < buffer2 and buffer1[1] > buffer2[1] and not (buffer1 > buffer2 and buffer1[1] < buffer2[1]))
sellCondition = conditional(buffer1 < buffer2 and buffer1[1] > buffer2[1] )

            plot_shape(
                (buyCondition),
                "AHORA!",
                shape_style.triangleup,
                shape_size.huge,
                colorBuy,
                shape_location.belowbar,
                -1,
                "AHORA!",
                "white"
               ) 

          plot_shape(
              (sellCondition),
                "AHORA!",
                shape_style.triangledown,
                shape_size.huge,
                colorSell,
                shape_location.abovebar,
                -1,
                "AHORA !",
                "white"
          )
 


--IQ OPTION SCRIPT HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--IQ OPTION SCRIPT HAOAN,
--SD 9870DFS DS87SDF BDSJBJSDF8 DFNS----IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--SDJKO3Q384EF8JSDFEESRJSDFFDSDFSD56D6843543SDF
--hgy&y*(&(&*(y9H78YG9U8HO8V6RfghyujgfjhfgCHBVKUYTKKBLLHBLIY--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4bnfgkguyloWOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--IQ OPTION SCRIPT HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--IQ OPTION SCRIPT HAOAN,
--SD 9870DFS DS87SDF BDSJBJSDF8 DFNS----IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--SDJKO3Q384EF8JSDFEESRJSDFFDSDFSD56D6843543SDF
--hgy&y*(&(&*(y9H78YG9U8HO8V6RfghyujgfjhfgCHBVKUYTKKBLLHBLIY--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4bnfgkguyloWOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOdsdgvxcvIFSDFJFBNWE9RHIEF
--IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOdsdgvxcvIFSDFJFBNWE9RHIEF
-- start lines 
--colors
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDxcvxgdfSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--   
--IQ OPTION JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors
--linecolors 28739124   
--IQOPTION HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--IQOPTION JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--IQOPTION HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS-- 
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors ()JN6BT%R$%J()7654jHGGJGU$#@#$@#%$@#NMLKJHJCGRCH
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--           
-- start lines 
--colors
--linecolors 28739124   
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors ()JN6BT%R$%J()7654jHGGJGU$#@#$@#%$@#NMLKJHJCGRCH
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  -         
-- start lines 
--colors
--linecolors 28739124   
input_group {
    "Maxima",
    level_1_color = input { default = "red", type = input.color },
    level_1_width = input { default = 2, type = input.line_width }
}
--IQ OPTION SCRIPT HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--IQ OPTION SCRIPT HAOAN,
--SD 9870DFS DS87SDF BDSJBJSDF8 DFNS----IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--SDJKO3Q384EF8JSDFEESRJSDFFDSDFSD56D6843543SDF
--hgy&y*(&(&*(y9H78YG9U8HO8V6RfghyujgfjhfgCHBVKUYTKKBLLHBLIY--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4bnfgkguyloWOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
input_group {
    "Minima",
    level_2_color = input { default = "green", type = input.color },
    level_2_width = input { default = 2, type = input.line_width }
}
--IQ OPTION SCRIPT HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--IQ OPTION SCRIPT HAOAN,
--SD 9870DFS DS87SDF BDSJBJSDF8 DFNS----IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--SDJKO3Q384EF8JSDFEESRJSDFFDSDFSD56D6843543SDF
--hgy&y*(&(&*(y9H78YG9U8HO8V6RfghyujgfjhfgCHBVKUYTKKBLLHBLIY--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4bnfgkguyloWOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
local function m15(candle)
--IQ OPTION SCRIPT HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--IQ OPTION SCRIPT HAOAN,
--SD 9870DFS DS87SDF BDSJBJSDF8 DFNS----IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--SDJKO3Q384EF8JSDFEESRJSDFFDSDFSD56D6843543SDF
--hgy&y*(&(&*(y9H78YG9U8HO8V6RfghyujgfjhfgCHBVKUYTKKBLLHBLIY--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4bnfgkguyloWOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
    c1 = candle.high
    c2 = candle.low
end
--IQ OPTION SCRIPT HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--IQ OPTION SCRIPT HAOAN,
--SD 9870DFS DS87SDF BDSJBJSDF8 DFNS----IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--SDJKO3Q384EF8JSDFEESRJSDFFDSDFSD56D6843543SDF
--hgy&y*(&(&*(y9H78YG9U8HO8V6RfghyujgfjhfgCHBVKUYTKKBLLHBLIY--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4bnfgkguyloWOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
local methods = { m15 }
--IQ OPTION SCRIPT HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--IQ OPTION SCRIPT HAOAN,
--SD 9870DFS DS87SDF BDSJBJSDF8 DFNS----IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--SDJKO3Q384EF8JSDFEESRJSDFFDSDFSD56D6843543SDF
--hgy&y*(&(&*(y9H78YG9U8HO8V6RfghyujgfjhfgCHBVKUYTKKBLLHBLIY--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4bnfgkguyloWOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOdsdgvxcvIFSDFJFBNWE9RHIEF
--IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOdsdgvxcvIFSDFJFBNWE9RHIEF
-- start lines 
--colors
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDxcvxgdfSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--   
--IQ OPTION JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors
--linecolors 28739124   
--IQOPTION HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--IQOPTION JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--IQOPTION HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS-- 
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors ()JN6BT%R$%J()7654jHGGJGU$#@#$@#%$@#NMLKJHJCGRCH
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--           
-- start lines 
--colors
--linecolors 28739124   
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors ()JN6BT%R$%J()7654jHGGJGU$#@#$@#%$@#NMLKJHJCGRCH
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  -         
-- start lines 
--colors
--linecolors 28739124   
local resolution = "15m"
--IQ OPTION SCRIPT HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--IQ OPTION SCRIPT HAOAN,
--SD 9870DFS DS87SDF BDSJBJSDF8 DFNS----IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--SDJKO3Q384EF8JSDFEESRJSDFFDSDFSD56D6843543SDF
--hgy&y*(&(&*(y9H78YG9U8HO8V6RfghyujgfjhfgCHBVKUYTKKBLLHBLIY--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4bnfgkguyloWOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
sec = security (current_ticker_id, resolution)
--IQ OPTION SCRIPT HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--IQ OPTION SCRIPT HAOAN,
--SD 9870DFS DS87SDF BDSJBJSDF8 DFNS----IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--SDJKO3Q384EF8JSDFEESRJSDFFDSDFSD56D6843543SDF
--hgy&y*(&(&*(y9H78YG9U8HO8V6RfghyujgfjhfgCHBVKUYTKKBLLHBLIY--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4bnfgkguyloWOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOdsdgvxcvIFSDFJFBNWE9RHIEF
--IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOdsdgvxcvIFSDFJFBNWE9RHIEF
-- start lines 
--colors
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDxcvxgdfSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--   
--IQ OPTION JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors
--linecolors 28739124   
--IQOPTION HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--IQOPTION JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--IQOPTION HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS-- 
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors ()JN6BT%R$%J()7654jHGGJGU$#@#$@#%$@#NMLKJHJCGRCH
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--           
-- start lines 
--colors
--linecolors 28739124   
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4dgeh5WOIFSDFJFBNWE9RHIEF
-- start lines 
--colors ()JN6BT%R$%J()7654jHGGJGU$#@#$@#%$@#NMLKJHJCGRCH
--linecolors 28739124   
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--  -         
-- start lines 
--colors
--linecolors 28739124   
if sec then
   local method = methods [method_id]
   method (sec)
--IQ OPTION SCRIPT HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--IQ OPTION SCRIPT HAOAN,
--SD 9870DFS DS87SDF BDSJBJSDF8 DFNS----IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--SDJKO3Q384EF8JSDFEESRJSDFFDSDFSD56D6843543SDF
--hgy&y*(&(&*(y9H78YG9U8HO8V6RfghyujgfjhfgCHBVKUYTKKBLLHBLIY--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4bnfgkguyloWOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
   plot (c1, "C1",   level_1_color, level_1_width, 0, style.levels, na_mode.continue)
   plot (c2, "C2",   level_2_color, level_2_width, 0, style.levels, na_mode.continue) --IQ OPTION SCRIPT HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--IQ OPTION SCRIPT HAOAN,
--SD 9870DFS DS87SDF BDSJBJSDF8 DFNS----IQ OPTION LOGIN JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--SDJKO3Q384EF8JSDFEESRJSDFFDSDFSD56D6843543SDF
--hgy&y*(&(&*(y9H78YG9U8HO8V6RfghyujgfjhfgCHBVKUYTKKBLLHBLIY--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4bnfgkguyloWOIFSDFJFBNWE9RHIEF
--HAOAN,SD 9870DFS DS87SDF BDSJBJSDF8 DFNS--
--JNASDU8Q737YQ!@#$%&*()H9DS8AJDLKAMSDLKW4WOIFSDFJFBNWE9RHIEF 

end
