# html常用方法

##### 修改css3伪类值
``` html
<!-- html -->
<a href="javascript:;" data-val="555" class="upd-val"></a>
```
```css
/** css **/
.upd-val:after{
  content:attr(data-val);
}
```
``` javascript

//js修改值
$('.upd-val').data('val',666);

```
```html

#### 国际化手机验证

<select id="mySelect" name="phoneArea">
    <option value="1" data-pattern="^(86){0,1}1\d{10}$" check-key="^(86){0,1}1\d{10}$"
    data-code="86" class="tsl" data-phase-id="r_c_1">
        中国大陆 (+86)
    </option>
    <option value="2" data-pattern="^(00){0,1}(852){1}0{0,1}[1,5,6,9](?:\d{7}|\d{8}|\d{12})$"
    check-key="^(00){0,1}(852){1}0{0,1}[1,5,6,9](?:\d{7}|\d{8}|\d{12})$" data-code="852"
    class="tsl" data-phase-id="r_c_2">
        香港 (+852)
    </option>
    <option value="3" data-pattern="^(00){0,1}(853){1}6\d{7}$" check-key="^(00){0,1}(853){1}6\d{7}$"
    data-code="853" class="tsl" data-phase-id="r_c_3">
        澳门 (+853)
    </option>
    <option value="4" data-pattern="^(00){0,1}(886){1}0{0,1}[6,7,9](?:\d{7}|\d{8}|\d{10})$"
    check-key="^(00){0,1}(886){1}0{0,1}[6,7,9](?:\d{7}|\d{8}|\d{10})$" data-code="886"
    class="tsl" data-phase-id="r_c_4">
        台湾 (+886)
    </option>
    <option value="5" data-pattern="^(00){0,1}(82){1}0{0,1}[7,1](?:\d{8}|\d{9})$"
    check-key="^(00){0,1}(82){1}0{0,1}[7,1](?:\d{8}|\d{9})$" data-code="82"
    class="tsl" data-phase-id="r_c_5">
        韩国 (+82)
    </option>
    <option value="6" data-pattern="^(00){0,1}(81){1}0{0,1}[7,8,9](?:\d{8}|\d{9})$"
    check-key="^(00){0,1}(81){1}0{0,1}[7,8,9](?:\d{8}|\d{9})$" data-code="81"
    class="tsl" data-phase-id="r_c_6">
        日本 (+81)
    </option>
    <option value="7" data-pattern="^(00){0,1}(1){1}\d{10,12}$" check-key="^(00){0,1}(1){1}\d{10,12}$"
    data-code="1" class="tsl" data-phase-id="r_c_7">
        美国 (+1)
    </option>
    <option value="8" data-pattern="^(00){0,1}(1){1}\d{10}$" check-key="^(00){0,1}(1){1}\d{10}$"
    data-code="1" class="tsl" data-phase-id="r_c_8">
        加拿大 (+1)
    </option>
    <option value="9" data-pattern="^(00){0,1}(44){1}[347-9](\d{8,9}|\d{11,12})$"
    check-key="^(00){0,1}(44){1}[347-9](\d{8,9}|\d{11,12})$" data-code="44"
    class="tsl" data-phase-id="r_c_9">
        英国 (+44)
    </option>
    <option value="10" data-pattern="^(00){0,1}(61){1}4\d{8,9}$" check-key="^(00){0,1}(61){1}4\d{8,9}$"
    data-code="61" class="tsl" data-phase-id="r_c_10">
        澳大利亚 (+61)
    </option>
    <option value="11" data-pattern="^(00){0,1}(65){1}[13689]\d{6,7}$" check-key="^(00){0,1}(65){1}[13689]\d{6,7}$"
    data-code="65" class="tsl" data-phase-id="r_c_11">
        新加坡 (+65)
    </option>
    <option value="12" data-pattern="^(00){0,1}(60){1}1\d{8,9}$" check-key="^(00){0,1}(60){1}1\d{8,9}$"
    data-code="60" class="tsl" data-phase-id="r_c_12">
        马来西亚 (+60)
    </option>
    <option value="13" data-pattern="^(00){0,1}(66){1}[13456789]\d{7,8}$"
    check-key="^(00){0,1}(66){1}[13456789]\d{7,8}$" data-code="66" class="tsl"
    data-phase-id="r_c_13">
        泰国 (+66)
    </option>
    <option value="14" data-pattern="^(00){0,1}(84){1}[1-9]\d{6,9}$" check-key="^(00){0,1}(84){1}[1-9]\d{6,9}$"
    data-code="84" class="tsl" data-phase-id="r_c_14">
        越南 (+84)
    </option>
    <option value="15" data-pattern="^(00){0,1}(63){1}[24579](\d{7,9}|\d{12})$"
    check-key="^(00){0,1}(63){1}[24579](\d{7,9}|\d{12})$" data-code="63" class="tsl"
    data-phase-id="r_c_15">
        菲律宾 (+63)
    </option>
    <option value="16" data-pattern="^(00){0,1}(62){1}[2-9]\d{7,11}$" check-key="^(00){0,1}(62){1}[2-9]\d{7,11}$"
    data-code="62" class="tsl" data-phase-id="r_c_16">
        印度尼西亚 (+62)
    </option>
    <option value="17" data-pattern="^(00){0,1}(49){1}1(\d{5,6}|\d{9,12})$"
    check-key="^(00){0,1}(49){1}1(\d{5,6}|\d{9,12})$" data-code="49" class="tsl"
    data-phase-id="r_c_17">
        德国 (+49)
    </option>
    <option value="18" data-pattern="^(00){0,1}(39){1}[37]\d{8,11}$" check-key="^(00){0,1}(39){1}[37]\d{8,11}$"
    data-code="39" class="tsl" data-phase-id="r_c_18">
        意大利 (+39)
    </option>
    <option value="19" data-pattern="^(00){0,1}(33){1}(\d{6}|\d{8,9})$" check-key="^(00){0,1}(33){1}(\d{6}|\d{8,9})$"
    data-code="33" class="tsl" data-phase-id="r_c_19">
        法国 (+33)
    </option>
    <option value="20" data-pattern="^(00){0,1}(7){1}[13489]\d{9,11}$" check-key="^(00){0,1}(7){1}[13489]\d{9,11}$"
    data-code="7" class="tsl" data-phase-id="r_c_20">
        俄罗斯 (+7)
    </option>
    <option value="21" data-pattern="^(00){0,1}(64){1}[278]\d{7,9}$" check-key="^(00){0,1}(64){1}[278]\d{7,9}$"
    data-code="64" class="tsl" data-phase-id="r_c_21">
        新西兰 (+64)
    </option>
    <option value="22" data-pattern="^(00){0,1}(31){1}6\d{8}$" check-key="^(00){0,1}(31){1}6\d{8}$"
    data-code="31" class="tsl" data-phase-id="r_c_22">
        荷兰 (+31)
    </option>
    <option value="23" data-pattern="^(00){0,1}(46){1}[124-7](\d{8}|\d{10}|\d{12})$"
    check-key="^(00){0,1}(46){1}[124-7](\d{8}|\d{10}|\d{12})$" data-code="46"
    class="tsl" data-phase-id="r_c_23">
        瑞典 (+46)
    </option>
    <option value="24" data-pattern="^(00){0,1}(380){1}[3-79]\d{8,9}$" check-key="^(00){0,1}(380){1}[3-79]\d{8,9}$"
    data-code="380" class="tsl" data-phase-id="r_c_24">
        乌克兰 (+380)
    </option>
    <option value="25" data-pattern="^(00){0,1}(971){1}\d{6,12}$" check-key="^(00){0,1}(971){1}\d{6,12}$"
    data-code="971" class="tsl" data-phase-id="r_c_25">
        阿联酋 (+971)
    </option>
    <option value="26" data-pattern="^(00){0,1}(54){1}\d{6,12}$" check-key="^(00){0,1}(54){1}\d{6,12}$"
    data-code="54" class="tsl" data-phase-id="r_c_26">
        阿根廷 (+54)
    </option>
    <option value="27" data-pattern="^(00){0,1}(43){1}\d{6,12}$" check-key="^(00){0,1}(43){1}\d{6,12}$"
    data-code="43" class="tsl" data-phase-id="r_c_27">
        奥地利 (+43)
    </option>
    <option value="28" data-pattern="^(00){0,1}(32){1}\d{6,12}$" check-key="^(00){0,1}(32){1}\d{6,12}$"
    data-code="32" class="tsl" data-phase-id="r_c_28">
        比利时 (+32)
    </option>
    <option value="29" data-pattern="^(00){0,1}(359){1}\d{6,12}$" check-key="^(00){0,1}(359){1}\d{6,12}$"
    data-code="359" class="tsl" data-phase-id="r_c_29">
        保加利亚 (+359)
    </option>
    <option value="30" data-pattern="^(00){0,1}(55){1}\d{6,12}$" check-key="^(00){0,1}(55){1}\d{6,12}$"
    data-code="55" class="tsl" data-phase-id="r_c_30">
        巴西 (+55)
    </option>
    <option value="31" data-pattern="^(00){0,1}(1242){1}\d{6,12}$" check-key="^(00){0,1}(1242){1}\d{6,12}$"
    data-code="1242" class="tsl" data-phase-id="r_c_31">
        巴哈马 (+1242)
    </option>
    <option value="32" data-pattern="^(00){0,1}(375){1}\d{6,12}$" check-key="^(00){0,1}(375){1}\d{6,12}$"
    data-code="375" class="tsl" data-phase-id="r_c_32">
        白俄罗斯 (+375)
    </option>
    <option value="33" data-pattern="^(00){0,1}(501){1}\d{6,12}$" check-key="^(00){0,1}(501){1}\d{6,12}$"
    data-code="501" class="tsl" data-phase-id="r_c_33">
        伯利兹 (+501)
    </option>
    <option value="34" data-pattern="^(00){0,1}(41){1}\d{6,12}$" check-key="^(00){0,1}(41){1}\d{6,12}$"
    data-code="41" class="tsl" data-phase-id="r_c_34">
        瑞士 (+41)
    </option>
    <option value="35" data-pattern="^(00){0,1}(56){1}\d{6,12}$" check-key="^(00){0,1}(56){1}\d{6,12}$"
    data-code="56" class="tsl" data-phase-id="r_c_35">
        智利 (+56)
    </option>
    <option value="36" data-pattern="^(00){0,1}(57){1}\d{6,12}$" check-key="^(00){0,1}(57){1}\d{6,12}$"
    data-code="57" class="tsl" data-phase-id="r_c_36">
        哥伦比亚 (+57)
    </option>
    <option value="37" data-pattern="^(00){0,1}(45){1}\d{6,12}$" check-key="^(00){0,1}(45){1}\d{6,12}$"
    data-code="45" class="tsl" data-phase-id="r_c_37">
        丹麦 (+45)
    </option>
    <option value="38" data-pattern="^(00){0,1}(372){1}\d{6,12}$" check-key="^(00){0,1}(372){1}\d{6,12}$"
    data-code="372" class="tsl" data-phase-id="r_c_38">
        爱沙尼亚 (+372)
    </option>
    <option value="39" data-pattern="^(00){0,1}(20){1}\d{6,12}$" check-key="^(00){0,1}(20){1}\d{6,12}$"
    data-code="20" class="tsl" data-phase-id="r_c_39">
        埃及 (+20)
    </option>
    <option value="40" data-pattern="^(00){0,1}(34){1}\d{6,12}$" check-key="^(00){0,1}(34){1}\d{6,12}$"
    data-code="34" class="tsl" data-phase-id="r_c_40">
        西班牙 (+34)
    </option>
    <option value="41" data-pattern="^(00){0,1}(358){1}\d{6,12}$" check-key="^(00){0,1}(358){1}\d{6,12}$"
    data-code="358" class="tsl" data-phase-id="r_c_41">
        芬兰 (+358)
    </option>
    <option value="42" data-pattern="^(00){0,1}(30){1}\d{6,12}$" check-key="^(00){0,1}(30){1}\d{6,12}$"
    data-code="30" class="tsl" data-phase-id="r_c_42">
        希腊 (+30)
    </option>
    <option value="43" data-pattern="^(00){0,1}(36){1}\d{6,12}$" check-key="^(00){0,1}(36){1}\d{6,12}$"
    data-code="36" class="tsl" data-phase-id="r_c_43">
        匈牙利 (+36)
    </option>
    <option value="44" data-pattern="^(00){0,1}(353){1}\d{6,12}$" check-key="^(00){0,1}(353){1}\d{6,12}$"
    data-code="353" class="tsl" data-phase-id="r_c_44">
        爱尔兰 (+353)
    </option>
    <option value="45" data-pattern="^(00){0,1}(972){1}\d{6,12}$" check-key="^(00){0,1}(972){1}\d{6,12}$"
    data-code="972" class="tsl" data-phase-id="r_c_45">
        以色列 (+972)
    </option>
    <option value="46" data-pattern="^(00){0,1}(91){1}\d{6,12}$" check-key="^(00){0,1}(91){1}\d{6,12}$"
    data-code="91" class="tsl" data-phase-id="r_c_46">
        印度 (+91)
    </option>
    <option value="47" data-pattern="^(00){0,1}(962){1}\d{6,12}$" check-key="^(00){0,1}(962){1}\d{6,12}$"
    data-code="962" class="tsl" data-phase-id="r_c_47">
        约旦 (+962)
    </option>
    <option value="48" data-pattern="^(00){0,1}(996){1}\d{6,12}$" check-key="^(00){0,1}(996){1}\d{6,12}$"
    data-code="996" class="tsl" data-phase-id="r_c_48">
        吉尔吉斯斯坦 (+996)
    </option>
    <option value="49" data-pattern="^(00){0,1}(855){1}\d{6,12}$" check-key="^(00){0,1}(855){1}\d{6,12}$"
    data-code="855" class="tsl" data-phase-id="r_c_49">
        柬埔寨 (+855)
    </option>
    <option value="50" data-pattern="^(00){0,1}(94){1}\d{6,12}$" check-key="^(00){0,1}(94){1}\d{6,12}$"
    data-code="94" class="tsl" data-phase-id="r_c_50">
        斯里兰卡 (+94)
    </option>
    <option value="51" data-pattern="^(00){0,1}(370){1}\d{6,12}$" check-key="^(00){0,1}(370){1}\d{6,12}$"
    data-code="370" class="tsl" data-phase-id="r_c_51">
        立陶宛 (+370)
    </option>
    <option value="52" data-pattern="^(00){0,1}(352){1}\d{6,12}$" check-key="^(00){0,1}(352){1}\d{6,12}$"
    data-code="352" class="tsl" data-phase-id="r_c_52">
        卢森堡 (+352)
    </option>
    <option value="53" data-pattern="^(00){0,1}(212){1}\d{6,12}$" check-key="^(00){0,1}(212){1}\d{6,12}$"
    data-code="212" class="tsl" data-phase-id="r_c_53">
        摩洛哥 (+212)
    </option>
    <option value="54" data-pattern="^(00){0,1}(976){1}\d{6,12}$" check-key="^(00){0,1}(976){1}\d{6,12}$"
    data-code="976" class="tsl" data-phase-id="r_c_54">
        蒙古 (+976)
    </option>
    <option value="55" data-pattern="^(00){0,1}(960){1}\d{6,12}$" check-key="^(00){0,1}(960){1}\d{6,12}$"
    data-code="960" class="tsl" data-phase-id="r_c_55">
        马尔代夫 (+960)
    </option>
    <option value="56" data-pattern="^(00){0,1}(52){1}\d{6,12}$" check-key="^(00){0,1}(52){1}\d{6,12}$"
    data-code="52" class="tsl" data-phase-id="r_c_56">
        墨西哥 (+52)
    </option>
    <option value="57" data-pattern="^(00){0,1}(234){1}\d{6,12}$" check-key="^(00){0,1}(234){1}\d{6,12}$"
    data-code="234" class="tsl" data-phase-id="r_c_57">
        尼日利亚 (+234)
    </option>
    <option value="58" data-pattern="^(00){0,1}(47){1}\d{6,12}$" check-key="^(00){0,1}(47){1}\d{6,12}$"
    data-code="47" class="tsl" data-phase-id="r_c_58">
        挪威 (+47)
    </option>
    <option value="59" data-pattern="^(00){0,1}(507){1}\d{6,12}$" check-key="^(00){0,1}(507){1}\d{6,12}$"
    data-code="507" class="tsl" data-phase-id="r_c_59">
        巴拿马 (+507)
    </option>
    <option value="60" data-pattern="^(00){0,1}(51){1}\d{6,12}$" check-key="^(00){0,1}(51){1}\d{6,12}$"
    data-code="51" class="tsl" data-phase-id="r_c_60">
        秘鲁 (+51)
    </option>
    <option value="61" data-pattern="^(00){0,1}(48){1}\d{6,12}$" check-key="^(00){0,1}(48){1}\d{6,12}$"
    data-code="48" class="tsl" data-phase-id="r_c_61">
        波兰 (+48)
    </option>
    <option value="62" data-pattern="^(00){0,1}(351){1}\d{6,12}$" check-key="^(00){0,1}(351){1}\d{6,12}$"
    data-code="351" class="tsl" data-phase-id="r_c_62">
        葡萄牙 (+351)
    </option>
    <option value="63" data-pattern="^(00){0,1}(974){1}\d{6,12}$" check-key="^(00){0,1}(974){1}\d{6,12}$"
    data-code="974" class="tsl" data-phase-id="r_c_63">
        卡塔尔 (+974)
    </option>
    <option value="64" data-pattern="^(00){0,1}(40){1}\d{6,12}$" check-key="^(00){0,1}(40){1}\d{6,12}$"
    data-code="40" class="tsl" data-phase-id="r_c_64">
        罗马尼亚 (+40)
    </option>
    <option value="65" data-pattern="^(00){0,1}(381){1}\d{6,12}$" check-key="^(00){0,1}(381){1}\d{6,12}$"
    data-code="381" class="tsl" data-phase-id="r_c_65">
        塞尔维亚 (+381)
    </option>
    <option value="66" data-pattern="^(00){0,1}(966){1}\d{6,12}$" check-key="^(00){0,1}(966){1}\d{6,12}$"
    data-code="966" class="tsl" data-phase-id="r_c_66">
        沙特阿拉伯 (+966)
    </option>
    <option value="67" data-pattern="^(00){0,1}(248){1}\d{6,12}$" check-key="^(00){0,1}(248){1}\d{6,12}$"
    data-code="248" class="tsl" data-phase-id="r_c_67">
        塞舌尔 (+248)
    </option>
    <option value="68" data-pattern="^(00){0,1}(216){1}\d{6,12}$" check-key="^(00){0,1}(216){1}\d{6,12}$"
    data-code="216" class="tsl" data-phase-id="r_c_68">
        突尼斯 (+216)
    </option>
    <option value="69" data-pattern="^(00){0,1}(90){1}\d{6,12}$" check-key="^(00){0,1}(90){1}\d{6,12}$"
    data-code="90" class="tsl" data-phase-id="r_c_69">
        土耳其 (+90)
    </option>
    <option value="70" data-pattern="^(00){0,1}(58){1}\d{6,12}$" check-key="^(00){0,1}(58){1}\d{6,12}$"
    data-code="58" class="tsl" data-phase-id="r_c_70">
        委内瑞拉 (+58)
    </option>
    <option value="71" data-pattern="^(00){0,1}(1284){1}\d{6,12}$" check-key="^(00){0,1}(1284){1}\d{6,12}$"
    data-code="1284" class="tsl" data-phase-id="r_c_71">
        英属维尔京群岛 (+1284)
    </option>
    <option value="72" data-pattern="^(00){0,1}(27){1}\d{6,12}$" check-key="^(00){0,1}(27){1}\d{6,12}$"
    data-code="27" class="tsl" data-phase-id="r_c_72">
        南非 (+27)
    </option>
</select>
