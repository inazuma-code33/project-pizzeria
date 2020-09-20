
Problemy i rozwiązanie. 

Problem 1. Układ Plus min dodawanie ilosci i łaczenie cen - 
Rozwiązanie- Validac 
export class AmountWidget extends BaseWidget {
  constructor(wrapper){
    super(wrapper, settings.amountWidget.defaultValue);

    const thisWidget = this;

    thisWidget.getElements();
    thisWidget.initActions();

    //console.log('AmountWidget: ', thisWidget);
    //console.log('wrapper: ', wrapper);
  }
  getElements(){
    const thisWidget = this;

    thisWidget.dom.input = thisWidget.dom.wrapper.querySelector(
      select.widgets.amount.input
    );
    thisWidget.dom.linkDecrease = thisWidget.dom.wrapper.querySelector(
      select.widgets.amount.linkDecrease
    );
    thisWidget.dom.linkIncrease = thisWidget.dom.wrapper.querySelector(
      select.widgets.amount.linkIncrease
    );
  }
  isValid(newValue){
    return (
      !isNaN(newValue) &&
      newValue >= settings.amountWidget.defaultMin &&
      newValue <= settings.amountWidget.defaultMax
    );
  }
  initActions(){
    const thisWidget = this;

    thisWidget.dom.input.addEventListener('change', function(){
      thisWidget.value = thisWidget.dom.input.value;
    });
    thisWidget.dom.linkDecrease.addEventListener('click', function(event){
      event.preventDefault();
      thisWidget.value = --thisWidget.dom.input.value;
    });
    thisWidget.dom.linkIncrease.addEventListener('click', function(event){
      event.preventDefault();
      thisWidget.value = ++thisWidget.dom.input.value;
    });
  }
  renderValue(){
    const thisWidget = this;

    thisWidget.dom.input.value = thisWidget.value;
  }
}
Problem 2. Cart class, produkt cart class. 
Rozwiązanie 
class CartProduct{
  constructor(menuProduct, element){
    const thisCartProduct = this;
    Implementacja rozwiązania z sieci. 
    ZMiana Kodu HTML pod funkcje klas. 

    Projekt stwozony w oparciu o lekcje z Kursu Szkoły Kodilla oraz pomocy menotra i dobrej przyjaciółki :) 
