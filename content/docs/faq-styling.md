---
id: faq-styling
title: Stil ve CSS
permalink: docs/faq-styling.html
layout: docs
category: FAQ
---

### Bileşenlere CSS sınıflarını nasıl eklerim? {#how-do-i-add-css-classes-to-components}

Prop ile `className`'e metin gönderimi:

```jsx
render() {
  return <span className="menu navigation-menu">Menu</span>
}
```

Bileşenlere prop ya da state'leri yaygın bir şekildeki bağlanışı:

```jsx
render() {
  let className = 'menu';
  if (this.props.isActive) {
    className += ' menu-active';
  }
  return <span className={className}>Menu</span>
}
```

>İpucu
>
>Sık sık kendinize böyle bir kod yazarken bulursanız, [classnames](https://www.npmjs.com/package/classnames#usage-with-reactjs) basitleştirmeyi okuyunuz.

### Satır içi stilleri kullanabilir miyim? {#can-i-use-inline-styles}

Evet, [buradan](/docs/dom-elements.html#style) şekillendirme ile ilgili belgelere bakın .

### Satır içi stil kullanımı kötü mü? {#are-inline-styles-bad}

CSS sınıfları performans için satır içi stillerden daha iyidir.

### CSS-in-JS nedir? {#what-is-css-in-js}

"CSS-in-JS" CSS'in harici dosyalarda tanımlanmak yerine JavaScript kullanarak oluşturulduğu bir deseni ifade eder. JS'deki CSS kitaplıklarının karşılaştırmasını [buradan okuyun.](https://github.com/MicheleBertoli/css-in-js).

_Bu işlevselliğin React'in bir parçası olmadığını, ancak üçüncü taraf kütüphaneler tarafından sağlandığını unutmayın. React, stillerin nasıl tanımlanması gerektiği hakkında görüşe sahip değildir; Şüpheniz varsa, stillerinizi her zamanki gibi ayrı bir `*.css` dosyasında tanımlamak ve [`className`](/docs/dom-elements.html#classname) kullanarak bunlara başvurmak iyi bir başlangıç noktasıdır.

### React'te animasyon yapabilir miyim? {#can-i-do-animations-in-react}

React animasyonları güçlendirmek için kullanılabilir. Bakınız [React Transition Group](https://reactcommunity.org/react-transition-group/) ve [React Motion](https://github.com/chenglou/react-motion) ya da [React Spring](https://github.com/react-spring/react-spring), bunun için örnektir.
