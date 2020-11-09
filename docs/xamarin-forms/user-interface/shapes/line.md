---
title: "Xamarin.Forms Shapes: Line"
description: "The Xamarin.Forms Line class can be used to draw lines."
ms.prod: xamarin
ms.assetid: 384F1A72-6D3B-4FD3-BC40-E00A73A463EC
ms.technology: xamarin-forms
author: davidbritch
ms.author: dabritch
ms.date: 06/20/2020
no-loc: [Xamarin.Forms, Xamarin.Essentials]
---

# Xamarin.Forms Shapes: Line

![Pre-release API](~/media/shared/preview.png)

[![Download Sample](~/media/shared/download.png) Download the sample](/samples/xamarin/xamarin-forms-samples/userinterface-shapesdemos/)

The `Line` class derives from the `Shape` class, and can be used to draw lines. For information on the properties that the `Line` class inherits from the `Shape` class, see [Xamarin.Forms Shapes](index.md).

`Line` defines the following properties:

- `X1`, of type double, indicates the x-coordinate of the start point of the line. The default value of this property is 0.0.
- `Y1`, of type double, indicates the y-coordinate of the start point of the line. The default value of this property is 0.0.
- `X2`, of type double, indicates the x-coordinate of the end point of the line. The default value of this property is 0.0.
- `Y2`, of type double, indicates the y-coordinate of the end point of the line. The default value of this property is 0.0.

These properties are backed by [`BindableProperty`](xref:Xamarin.Forms.BindableProperty) objects, which means that they can be targets of data bindings, and styled.

For information about controlling how line ends are drawn, see [Control line ends](index.md#control-line-ends).

## Create a Line

To draw a line, create a `Line` object and set its `X1` and `Y1` properties to its start point, and its `X2` and `Y2` properties to its end point. In addition, set its `Stroke` property to a [`Color`](xref:Xamarin.Forms.Color) because a line without a stroke is invisible.

> [!NOTE]
> Setting the `Fill` property of a `Line` has no effect, because a line has no interior.

The following XAML example shows how to draw a line:

```xaml
<Line X1="40"
      Y1="0"
      X2="0"
      Y2="120"
      Stroke="Red"
      StrokeThickness="1" />
```

In this example, a red diagonal line is drawn from (40,0) to (0,120):

![Line](line-images/line.png "Line")

Because the `X1`, `Y1`, `X2`, and `Y2` properties have default values of 0, it's possible to draw some lines with minimal syntax:

```xaml
<Line Stroke="Red"
      StrokeThickness="1"
      X2="200" />
```

In this example, a horizontal line that's 200 device-independent units long is defined. Because the other properties are 0 by default, a line is drawn from (0,0) to (200,0).

The following XAML example shows how to draw a dashed line:

```xaml
<Line X1="40"
      Y1="0"
      X2="0"
      Y2="120"
      Stroke="DarkBlue"
      StrokeThickness="1"
      StrokeDashArray="1,1"
      StrokeDashOffset="6" />
```

In this example, a dark blue dashed diagonal line is drawn from (40,0) to (0,120):

![Dashed line](line-images/dashed-line.png "Dashed line")

For more information about drawing a dashed line, see [Draw dashed shapes](index.md#draw-dashed-shapes).

## Related links

- [ShapeDemos (sample)](/samples/xamarin/xamarin-forms-samples/userinterface-shapesdemos/)
- [Xamarin.Forms Shapes](index.md)
