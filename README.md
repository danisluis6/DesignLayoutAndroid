# DesignLayoutAndroid
## Create example for designing layout in Android.
=> If we want to put icon left to text in EditText?
+ Solution 1: Using drawable left
+ Solution 2: Put layout contain EditText and ImageView(ImageButton) on the left.

## We using TextInputLayout
=> TextInputLayout is actually EditText. It contains edittext.
+ Structure 1:
<LinearLayout/RelativeLayout>
  <EditText>
  <ImageView>(<ImageButton>)
</LinearLayout/RelativeLayout>

+ Structure 2:
<LinearLayout/RelativeLayout>
  <TextInputLayout>
    <EditText>(<AutoTextView>)
  </TextInputLayout>
  <ImageView>(<ImageButton>)
</LinearLayout/RelativeLayout>

## Problem with RadioGroup
+ Structure for layout
<RadioGroup>
  <RadioButton></RadioButton> (default by set checked = "true"
  <RadioButton></RadioButton> 
</RadioGroup>

+ How can we get value: 
====> new Object(RadioGroup) and use method getCheckedRadioButtonId() to return ID of RadioButton and compare.

## Interface and these solutions to apply it.
### Solution 1: 
A => I wana shoot Interface to B(Adapter, Activity or Fragment) 
=> Get data from B(But, Data come from process in B not constructor). How can I do that?
- [NEXT 1] Declare Interface.
- [NEXT 2] Specify event you will call in where?
- [THIS CASE] We will call in B.
- [NEXT 3] We will transfer Interface to B by these ways below
+ Way one: B.method(new Interface) 
+ Way two: A.constructor(new Interface) => Choose this way
- [NEXT 4] We create Interface to get Interface come from A in constructor or method.
- [NEXT 5] Find place to call event that you need to process like
