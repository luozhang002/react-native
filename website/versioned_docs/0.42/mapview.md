---
id: version-0.42-mapview
title: mapview
original_id: mapview
---
<a id="content"></a><h1><a class="anchor" name="mapview"></a>MapView <a class="hash-link" href="docs/mapview.html#mapview">#</a></h1><div><div><p><strong>IMPORTANT: This component is now DEPRECATED and will be removed
in January 2017 (React Native version 0.42). This component only supports
iOS.</strong></p><p><strong>Please use
<a href="https://github.com/airbnb/react-native-maps" target="_blank">react-native-maps</a> by Airbnb
instead of this component.</strong> Our friends at Airbnb have done an amazing job
building a cross-platform <code>MapView</code> component that is more feature
complete. It is used extensively (over 9k installs / month).</p><p><code>MapView</code> is used to display embeddable maps and annotations using
<code>MKMapView</code>.</p><div class="prism language-javascript">import React<span class="token punctuation">,</span> <span class="token punctuation">{</span> Component <span class="token punctuation">}</span> from <span class="token string">'react'</span><span class="token punctuation">;</span>
import <span class="token punctuation">{</span> MapView <span class="token punctuation">}</span> from <span class="token string">'react-native'</span><span class="token punctuation">;</span>

class <span class="token class-name">MapMyRide</span> extends <span class="token class-name">Component</span> <span class="token punctuation">{</span>
  <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      &lt;MapView
        style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>height<span class="token punctuation">:</span> <span class="token number">200</span><span class="token punctuation">,</span> margin<span class="token punctuation">:</span> <span class="token number">40</span><span class="token punctuation">}</span><span class="token punctuation">}</span>
        showsUserLocation<span class="token operator">=</span><span class="token punctuation">{</span><span class="token boolean">true</span><span class="token punctuation">}</span>
      <span class="token operator">/</span><span class="token operator">&gt;</span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span></div></div><h3><a class="anchor" name="props"></a>Props <a class="hash-link" href="docs/mapview.html#props">#</a></h3><div class="props"><div class="prop"><h4 class="propTitle"><a class="anchor" name="view"></a><a href="docs/view.html#props">View props...</a> <a class="hash-link" href="docs/mapview.html#view">#</a></h4></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="annotations"></a>annotations?: <span class="propType"><span>[<span>{<span><span><span>latitude: number</span>, </span><span><span>longitude: number</span>, </span><span><span>animateDrop: bool</span>, </span><span><span>draggable: bool</span>, </span><span><span>onDragStateChange: function</span>, </span><span><span>onFocus: function</span>, </span><span><span>onBlur: function</span>, </span><span><span>title: string</span>, </span><span><span>subtitle: string</span>, </span><span><span>leftCalloutView: element</span>, </span><span><span>rightCalloutView: element</span>, </span><span><span>detailCalloutView: element</span>, </span><span><span>tintColor: <a href="docs/colors.html">color</a></span>, </span><span><span>image: Image.propTypes.source</span>, </span><span><span>view: element</span>, </span><span><span>id: string</span>, </span><span><span>hasLeftCallout: deprecatedPropType(
  React.PropTypes.bool,
  'Use `leftCalloutView` instead.'
)</span>, </span><span><span>hasRightCallout: deprecatedPropType(
  React.PropTypes.bool,
  'Use `rightCalloutView` instead.'
)</span>, </span><span><span>onLeftCalloutPress: deprecatedPropType(
  React.PropTypes.func,
  'Use `leftCalloutView` instead.'
)</span>, </span><span>onRightCalloutPress: deprecatedPropType(
  React.PropTypes.func,
  'Use `rightCalloutView` instead.'
)</span></span>}</span>]</span></span> <a class="hash-link" href="docs/mapview.html#annotations">#</a></h4><div><p>Map annotations with title and subtitle.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="followuserlocation"></a>followUserLocation?: <span class="propType">bool</span> <a class="hash-link" href="docs/mapview.html#followuserlocation">#</a></h4><div><p>If <code>true</code> the map will follow the user's location whenever it changes.
Note that this has no effect unless <code>showsUserLocation</code> is enabled.
Default value is <code>true</code>.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="legallabelinsets"></a>legalLabelInsets?: <span class="propType">{top: number, left: number, bottom: number, right: number}</span> <a class="hash-link" href="docs/mapview.html#legallabelinsets">#</a></h4><div><p>Insets for the map's legal label, originally at bottom left of the map.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="maptype"></a>mapType?: <span class="propType">enum('standard', 'satellite', 'hybrid')</span> <a class="hash-link" href="docs/mapview.html#maptype">#</a></h4><div><p>The map type to be displayed.</p><ul><li><code>standard</code>: Standard road map (default).</li><li><code>satellite</code>: Satellite view.</li><li><code>hybrid</code>: Satellite view with roads and points of interest overlaid.</li></ul></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="maxdelta"></a>maxDelta?: <span class="propType">number</span> <a class="hash-link" href="docs/mapview.html#maxdelta">#</a></h4><div><p>Maximum size of the area that can be displayed.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="mindelta"></a>minDelta?: <span class="propType">number</span> <a class="hash-link" href="docs/mapview.html#mindelta">#</a></h4><div><p>Minimum size of the area that can be displayed.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onannotationpress"></a>onAnnotationPress?: <span class="propType">function</span> <a class="hash-link" href="docs/mapview.html#onannotationpress">#</a></h4><div><p>Deprecated. Use annotation <code>onFocus</code> and <code>onBlur</code> instead.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onregionchange"></a>onRegionChange?: <span class="propType">function</span> <a class="hash-link" href="docs/mapview.html#onregionchange">#</a></h4><div><p>Callback that is called continuously when the user is dragging the map.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="onregionchangecomplete"></a>onRegionChangeComplete?: <span class="propType">function</span> <a class="hash-link" href="docs/mapview.html#onregionchangecomplete">#</a></h4><div><p>Callback that is called once, when the user is done moving the map.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="overlays"></a>overlays?: <span class="propType"><span>[<span>{<span><span><span>coordinates: <span>[<span>{<span><span><span>latitude: number</span>, </span><span>longitude: number</span></span>}</span>]</span></span>, </span><span><span>lineWidth: number</span>, </span><span><span>strokeColor: <a href="docs/colors.html">color</a></span>, </span><span><span>fillColor: <a href="docs/colors.html">color</a></span>, </span><span>id: string</span></span>}</span>]</span></span> <a class="hash-link" href="docs/mapview.html#overlays">#</a></h4><div><p>Map overlays</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="pitchenabled"></a>pitchEnabled?: <span class="propType">bool</span> <a class="hash-link" href="docs/mapview.html#pitchenabled">#</a></h4><div><p>When this property is set to <code>true</code> and a valid camera is associated
with the map, the camera's pitch angle is used to tilt the plane
of the map.</p><p>When this property is set to <code>false</code>, the camera's pitch
angle is ignored and the map is always displayed as if the user
is looking straight down onto it.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="region"></a>region?: <span class="propType"><span>{<span><span><span>latitude: number</span>, </span><span><span>longitude: number</span>, </span><span><span>latitudeDelta: number</span>, </span><span>longitudeDelta: number</span></span>}</span></span> <a class="hash-link" href="docs/mapview.html#region">#</a></h4><div><p>The region to be displayed by the map.</p><p>The region is defined by the center coordinates and the span of
coordinates to display.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="rotateenabled"></a>rotateEnabled?: <span class="propType">bool</span> <a class="hash-link" href="docs/mapview.html#rotateenabled">#</a></h4><div><p>When this property is set to <code>true</code> and a valid camera is associated with
the map, the camera's heading angle is used to rotate the plane of the
map around its center point.</p><p>When this property is set to <code>false</code>, the
camera's heading angle is ignored and the map is always oriented so
that true north is situated at the top of the map view</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="scrollenabled"></a>scrollEnabled?: <span class="propType">bool</span> <a class="hash-link" href="docs/mapview.html#scrollenabled">#</a></h4><div><p>If <code>false</code> the user won't be able to change the map region being displayed.
Default value is <code>true</code>.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="showsannotationcallouts"></a>showsAnnotationCallouts?: <span class="propType">bool</span> <a class="hash-link" href="docs/mapview.html#showsannotationcallouts">#</a></h4><div><p>If <code>true</code> the map will show the callouts for all annotations without
the user having to click on the annotation.
Default value is <code>false</code>.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="showscompass"></a>showsCompass?: <span class="propType">bool</span> <a class="hash-link" href="docs/mapview.html#showscompass">#</a></h4><div><p>If <code>false</code>, compass won't be displayed on the map.
Default value is <code>true</code>.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="showspointsofinterest"></a>showsPointsOfInterest?: <span class="propType">bool</span> <a class="hash-link" href="docs/mapview.html#showspointsofinterest">#</a></h4><div><p>If <code>false</code> points of interest won't be displayed on the map.
Default value is <code>true</code>.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="showsuserlocation"></a>showsUserLocation?: <span class="propType">bool</span> <a class="hash-link" href="docs/mapview.html#showsuserlocation">#</a></h4><div><p>If <code>true</code> the app will ask for the user's location and display it on
the map. Default value is <code>false</code>.</p><p><strong>NOTE</strong>: You'll need to add the <code>NSLocationWhenInUseUsageDescription</code>
key in Info.plist to enable geolocation, otherwise it will fail silently.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="style"></a>style?: <span class="propType"><a href="docs/view.html#style">View#style</a></span> <a class="hash-link" href="docs/mapview.html#style">#</a></h4><div><p>Used to style and layout the <code>MapView</code>.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="zoomenabled"></a>zoomEnabled?: <span class="propType">bool</span> <a class="hash-link" href="docs/mapview.html#zoomenabled">#</a></h4><div><p>If <code>false</code> the user won't be able to pinch/zoom the map.
Default value is <code>true</code>.</p></div></div><div class="prop"><h4 class="propTitle"><a class="anchor" name="active"></a><span class="platform">android</span>active?: <span class="propType">bool</span> <a class="hash-link" href="docs/mapview.html#active">#</a></h4></div></div><span><h3><a class="anchor" name="type-definitions"></a>Type Definitions <a class="hash-link" href="docs/mapview.html#type-definitions">#</a></h3><div class="props"><div class="prop"><h4 class="propTitle"><a class="anchor" name="annotationdragstate"></a>AnnotationDragState <a class="hash-link" href="docs/mapview.html#annotationdragstate">#</a></h4><div><p>State of an annotation on the map.</p></div><strong>Type:</strong><br>$Enum<div><br><strong>Constants:</strong><table class="params"><thead><tr><th>Value</th><th>Description</th></tr></thead><tbody><tr><td>idle</td><td class="description"><div><p>Annotation is not being touched.</p></div></td></tr><tr><td>starting</td><td class="description"><div><p>Annotation dragging has began.</p></div></td></tr><tr><td>dragging</td><td class="description"><div><p>Annotation is being dragged.</p></div></td></tr><tr><td>canceling</td><td class="description"><div><p>Annotation dragging is being canceled.</p></div></td></tr><tr><td>ending</td><td class="description"><div><p>Annotation dragging has ended.</p></div></td></tr></tbody></table></div></div></div></span></div><p class="edit-page-block">You can <a target="_blank" href="https://github.com/facebook/react-native/blob/master/Libraries/Components/MapView/MapView.js">edit the content above on GitHub</a> and send us a pull request!</p><div><div><table width="100%"><tbody><tr><td><h3><a class="anchor" name="examples"></a>Examples <a class="hash-link" href="docs/mapview.html#examples">#</a></h3></td><td style="text-align:right;"><a target="_blank" href="https://github.com/facebook/react-native/blob/master/Examples/UIExplorer/js/MapViewExample.js">Edit on GitHub</a></td></tr></tbody></table><div class="example-container"><div class="prism language-javascript"><span class="token string">'use strict'</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> React <span class="token operator">=</span> <span class="token function">require<span class="token punctuation">(</span></span><span class="token string">'react'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> ReactNative <span class="token operator">=</span> <span class="token function">require<span class="token punctuation">(</span></span><span class="token string">'react-native'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token keyword">var</span> <span class="token punctuation">{</span> PropTypes <span class="token punctuation">}</span> <span class="token operator">=</span> React<span class="token punctuation">;</span>
<span class="token keyword">var</span> <span class="token punctuation">{</span>
  Image<span class="token punctuation">,</span>
  MapView<span class="token punctuation">,</span>
  StyleSheet<span class="token punctuation">,</span>
  Text<span class="token punctuation">,</span>
  TextInput<span class="token punctuation">,</span>
  TouchableOpacity<span class="token punctuation">,</span>
  View<span class="token punctuation">,</span>
<span class="token punctuation">}</span> <span class="token operator">=</span> ReactNative<span class="token punctuation">;</span>

<span class="token keyword">var</span> regionText <span class="token operator">=</span> <span class="token punctuation">{</span>
  latitude<span class="token punctuation">:</span> <span class="token string">'0'</span><span class="token punctuation">,</span>
  longitude<span class="token punctuation">:</span> <span class="token string">'0'</span><span class="token punctuation">,</span>
  latitudeDelta<span class="token punctuation">:</span> <span class="token string">'0'</span><span class="token punctuation">,</span>
  longitudeDelta<span class="token punctuation">:</span> <span class="token string">'0'</span><span class="token punctuation">,</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>

<span class="token keyword">var</span> MapRegionInput <span class="token operator">=</span> React<span class="token punctuation">.</span><span class="token function">createClass<span class="token punctuation">(</span></span><span class="token punctuation">{</span>

  propTypes<span class="token punctuation">:</span> <span class="token punctuation">{</span>
    region<span class="token punctuation">:</span> PropTypes<span class="token punctuation">.</span><span class="token function">shape<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
      latitude<span class="token punctuation">:</span> PropTypes<span class="token punctuation">.</span>number<span class="token punctuation">.</span>isRequired<span class="token punctuation">,</span>
      longitude<span class="token punctuation">:</span> PropTypes<span class="token punctuation">.</span>number<span class="token punctuation">.</span>isRequired<span class="token punctuation">,</span>
      latitudeDelta<span class="token punctuation">:</span> PropTypes<span class="token punctuation">.</span>number<span class="token punctuation">,</span>
      longitudeDelta<span class="token punctuation">:</span> PropTypes<span class="token punctuation">.</span>number<span class="token punctuation">,</span>
    <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
    onChange<span class="token punctuation">:</span> PropTypes<span class="token punctuation">.</span>func<span class="token punctuation">.</span>isRequired<span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  <span class="token function">getInitialState<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">{</span>
      region<span class="token punctuation">:</span> <span class="token punctuation">{</span>
        latitude<span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
        longitude<span class="token punctuation">:</span> <span class="token number">0</span><span class="token punctuation">,</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">}</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  componentWillReceiveProps<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span>nextProps<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
      region<span class="token punctuation">:</span> nextProps<span class="token punctuation">.</span>region <span class="token operator">||</span> <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">getInitialState<span class="token punctuation">(</span></span><span class="token punctuation">)</span><span class="token punctuation">.</span>region
    <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  render<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">var</span> region <span class="token operator">=</span> <span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>region <span class="token operator">||</span> <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">getInitialState<span class="token punctuation">(</span></span><span class="token punctuation">)</span><span class="token punctuation">.</span>region<span class="token punctuation">;</span>
    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      &lt;View<span class="token operator">&gt;</span>
        &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>row<span class="token punctuation">}</span><span class="token operator">&gt;</span>
          &lt;Text<span class="token operator">&gt;</span>
            <span class="token punctuation">{</span><span class="token string">'Latitude'</span><span class="token punctuation">}</span>
          &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
          &lt;TextInput
            value<span class="token operator">=</span><span class="token punctuation">{</span><span class="token string">''</span> <span class="token operator">+</span> region<span class="token punctuation">.</span>latitude<span class="token punctuation">}</span>
            style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>textInput<span class="token punctuation">}</span>
            onChange<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>_onChangeLatitude<span class="token punctuation">}</span>
            selectTextOnFocus<span class="token operator">=</span><span class="token punctuation">{</span><span class="token boolean">true</span><span class="token punctuation">}</span>
          <span class="token operator">/</span><span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
        &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>row<span class="token punctuation">}</span><span class="token operator">&gt;</span>
          &lt;Text<span class="token operator">&gt;</span>
            <span class="token punctuation">{</span><span class="token string">'Longitude'</span><span class="token punctuation">}</span>
          &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
          &lt;TextInput
            value<span class="token operator">=</span><span class="token punctuation">{</span><span class="token string">''</span> <span class="token operator">+</span> region<span class="token punctuation">.</span>longitude<span class="token punctuation">}</span>
            style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>textInput<span class="token punctuation">}</span>
            onChange<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>_onChangeLongitude<span class="token punctuation">}</span>
            selectTextOnFocus<span class="token operator">=</span><span class="token punctuation">{</span><span class="token boolean">true</span><span class="token punctuation">}</span>
          <span class="token operator">/</span><span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
        &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>row<span class="token punctuation">}</span><span class="token operator">&gt;</span>
          &lt;Text<span class="token operator">&gt;</span>
            <span class="token punctuation">{</span><span class="token string">'Latitude delta'</span><span class="token punctuation">}</span>
          &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
          &lt;TextInput
            value<span class="token operator">=</span><span class="token punctuation">{</span>
              region<span class="token punctuation">.</span>latitudeDelta <span class="token operator">==</span> <span class="token keyword">null</span> <span class="token operator">?</span> <span class="token string">''</span> <span class="token punctuation">:</span> <span class="token function">String<span class="token punctuation">(</span></span>region<span class="token punctuation">.</span>latitudeDelta<span class="token punctuation">)</span>
            <span class="token punctuation">}</span>
            style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>textInput<span class="token punctuation">}</span>
            onChange<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>_onChangeLatitudeDelta<span class="token punctuation">}</span>
            selectTextOnFocus<span class="token operator">=</span><span class="token punctuation">{</span><span class="token boolean">true</span><span class="token punctuation">}</span>
          <span class="token operator">/</span><span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
        &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>row<span class="token punctuation">}</span><span class="token operator">&gt;</span>
          &lt;Text<span class="token operator">&gt;</span>
            <span class="token punctuation">{</span><span class="token string">'Longitude delta'</span><span class="token punctuation">}</span>
          &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
          &lt;TextInput
            value<span class="token operator">=</span><span class="token punctuation">{</span>
              region<span class="token punctuation">.</span>longitudeDelta <span class="token operator">==</span> <span class="token keyword">null</span> <span class="token operator">?</span> <span class="token string">''</span> <span class="token punctuation">:</span> <span class="token function">String<span class="token punctuation">(</span></span>region<span class="token punctuation">.</span>longitudeDelta<span class="token punctuation">)</span>
            <span class="token punctuation">}</span>
            style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>textInput<span class="token punctuation">}</span>
            onChange<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>_onChangeLongitudeDelta<span class="token punctuation">}</span>
            selectTextOnFocus<span class="token operator">=</span><span class="token punctuation">{</span><span class="token boolean">true</span><span class="token punctuation">}</span>
          <span class="token operator">/</span><span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
        &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>changeButton<span class="token punctuation">}</span><span class="token operator">&gt;</span>
          &lt;Text onPress<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>_change<span class="token punctuation">}</span><span class="token operator">&gt;</span>
            <span class="token punctuation">{</span><span class="token string">'Change'</span><span class="token punctuation">}</span>
          &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
      &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  _onChangeLatitude<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span>e<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    regionText<span class="token punctuation">.</span>latitude <span class="token operator">=</span> e<span class="token punctuation">.</span>nativeEvent<span class="token punctuation">.</span>text<span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  _onChangeLongitude<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span>e<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    regionText<span class="token punctuation">.</span>longitude <span class="token operator">=</span> e<span class="token punctuation">.</span>nativeEvent<span class="token punctuation">.</span>text<span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  _onChangeLatitudeDelta<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span>e<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    regionText<span class="token punctuation">.</span>latitudeDelta <span class="token operator">=</span> e<span class="token punctuation">.</span>nativeEvent<span class="token punctuation">.</span>text<span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  _onChangeLongitudeDelta<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span>e<span class="token punctuation">)</span> <span class="token punctuation">{</span>
    regionText<span class="token punctuation">.</span>longitudeDelta <span class="token operator">=</span> e<span class="token punctuation">.</span>nativeEvent<span class="token punctuation">.</span>text<span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

  _change<span class="token punctuation">:</span> <span class="token keyword">function</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
      region<span class="token punctuation">:</span> <span class="token punctuation">{</span>
        latitude<span class="token punctuation">:</span> <span class="token function">parseFloat<span class="token punctuation">(</span></span>regionText<span class="token punctuation">.</span>latitude<span class="token punctuation">)</span><span class="token punctuation">,</span>
        longitude<span class="token punctuation">:</span> <span class="token function">parseFloat<span class="token punctuation">(</span></span>regionText<span class="token punctuation">.</span>longitude<span class="token punctuation">)</span><span class="token punctuation">,</span>
        latitudeDelta<span class="token punctuation">:</span> <span class="token function">parseFloat<span class="token punctuation">(</span></span>regionText<span class="token punctuation">.</span>latitudeDelta<span class="token punctuation">)</span><span class="token punctuation">,</span>
        longitudeDelta<span class="token punctuation">:</span> <span class="token function">parseFloat<span class="token punctuation">(</span></span>regionText<span class="token punctuation">.</span>longitudeDelta<span class="token punctuation">)</span><span class="token punctuation">,</span>
      <span class="token punctuation">}</span><span class="token punctuation">,</span>
    <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span><span class="token function">onChange<span class="token punctuation">(</span></span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>region<span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>

<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

class <span class="token class-name">MapViewExample</span> extends <span class="token class-name">React<span class="token punctuation">.</span>Component</span> <span class="token punctuation">{</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span>
    isFirstLoad<span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    mapRegion<span class="token punctuation">:</span> undefined<span class="token punctuation">,</span>
    mapRegionInput<span class="token punctuation">:</span> undefined<span class="token punctuation">,</span>
    annotations<span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      &lt;View<span class="token operator">&gt;</span>
        &lt;MapView
          style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>map<span class="token punctuation">}</span>
          onRegionChange<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>_onRegionChange<span class="token punctuation">}</span>
          onRegionChangeComplete<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>_onRegionChangeComplete<span class="token punctuation">}</span>
          region<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>mapRegion<span class="token punctuation">}</span>
          annotations<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>annotations<span class="token punctuation">}</span>
        <span class="token operator">/</span><span class="token operator">&gt;</span>
        &lt;MapRegionInput
          onChange<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>_onRegionInputChanged<span class="token punctuation">}</span>
          region<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>mapRegionInput<span class="token punctuation">}</span>
        <span class="token operator">/</span><span class="token operator">&gt;</span>
      &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>

  _getAnnotations <span class="token operator">=</span> <span class="token punctuation">(</span>region<span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">[</span><span class="token punctuation">{</span>
      longitude<span class="token punctuation">:</span> region<span class="token punctuation">.</span>longitude<span class="token punctuation">,</span>
      latitude<span class="token punctuation">:</span> region<span class="token punctuation">.</span>latitude<span class="token punctuation">,</span>
      title<span class="token punctuation">:</span> <span class="token string">'You Are Here'</span><span class="token punctuation">,</span>
    <span class="token punctuation">}</span><span class="token punctuation">]</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  _onRegionChange <span class="token operator">=</span> <span class="token punctuation">(</span>region<span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
      mapRegionInput<span class="token punctuation">:</span> region<span class="token punctuation">,</span>
    <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  _onRegionChangeComplete <span class="token operator">=</span> <span class="token punctuation">(</span>region<span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>isFirstLoad<span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
        mapRegionInput<span class="token punctuation">:</span> region<span class="token punctuation">,</span>
        annotations<span class="token punctuation">:</span> <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">_getAnnotations<span class="token punctuation">(</span></span>region<span class="token punctuation">)</span><span class="token punctuation">,</span>
        isFirstLoad<span class="token punctuation">:</span> <span class="token boolean">false</span><span class="token punctuation">,</span>
      <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  _onRegionInputChanged <span class="token operator">=</span> <span class="token punctuation">(</span>region<span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
    <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
      mapRegion<span class="token punctuation">:</span> region<span class="token punctuation">,</span>
      mapRegionInput<span class="token punctuation">:</span> region<span class="token punctuation">,</span>
      annotations<span class="token punctuation">:</span> <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">_getAnnotations<span class="token punctuation">(</span></span>region<span class="token punctuation">)</span><span class="token punctuation">,</span>
    <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

class <span class="token class-name">AnnotationExample</span> extends <span class="token class-name">React<span class="token punctuation">.</span>Component</span> <span class="token punctuation">{</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span>
    isFirstLoad<span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    annotations<span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
    mapRegion<span class="token punctuation">:</span> undefined<span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>isFirstLoad<span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">var</span> onRegionChangeComplete <span class="token operator">=</span> <span class="token punctuation">(</span>region<span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
        <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
          isFirstLoad<span class="token punctuation">:</span> <span class="token boolean">false</span><span class="token punctuation">,</span>
          annotations<span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">{</span>
            longitude<span class="token punctuation">:</span> region<span class="token punctuation">.</span>longitude<span class="token punctuation">,</span>
            latitude<span class="token punctuation">:</span> region<span class="token punctuation">.</span>latitude<span class="token punctuation">,</span>
            <span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>annotation<span class="token punctuation">,</span>
          <span class="token punctuation">}</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
        <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
      <span class="token punctuation">}</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>

    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      &lt;MapView
        showsAnnotationCallouts<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>props<span class="token punctuation">.</span>showsAnnotationCallouts<span class="token punctuation">}</span>
        style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>map<span class="token punctuation">}</span>
        onRegionChangeComplete<span class="token operator">=</span><span class="token punctuation">{</span>onRegionChangeComplete<span class="token punctuation">}</span>
        region<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>mapRegion<span class="token punctuation">}</span>
        annotations<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>annotations<span class="token punctuation">}</span>
      <span class="token operator">/</span><span class="token operator">&gt;</span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>

class <span class="token class-name">DraggableAnnotationExample</span> extends <span class="token class-name">React<span class="token punctuation">.</span>Component</span> <span class="token punctuation">{</span>
  state <span class="token operator">=</span> <span class="token punctuation">{</span>
    isFirstLoad<span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
    annotations<span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
    mapRegion<span class="token punctuation">:</span> undefined<span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  createAnnotation <span class="token operator">=</span> <span class="token punctuation">(</span>longitude<span class="token punctuation">,</span> latitude<span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
    <span class="token keyword">return</span> <span class="token punctuation">{</span>
      longitude<span class="token punctuation">,</span>
      latitude<span class="token punctuation">,</span>
      draggable<span class="token punctuation">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
      onDragStateChange<span class="token punctuation">:</span> <span class="token punctuation">(</span>event<span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
        <span class="token keyword">if</span> <span class="token punctuation">(</span>event<span class="token punctuation">.</span>state <span class="token operator">===</span> <span class="token string">'idle'</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
          <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
            annotations<span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">createAnnotation<span class="token punctuation">(</span></span>event<span class="token punctuation">.</span>longitude<span class="token punctuation">,</span> event<span class="token punctuation">.</span>latitude<span class="token punctuation">)</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
          <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
        console<span class="token punctuation">.</span><span class="token function">log<span class="token punctuation">(</span></span><span class="token string">'Drag state: '</span> <span class="token operator">+</span> event<span class="token punctuation">.</span>state<span class="token punctuation">)</span><span class="token punctuation">;</span>
      <span class="token punctuation">}</span><span class="token punctuation">,</span>
    <span class="token punctuation">}</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span><span class="token punctuation">;</span>

  <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    <span class="token keyword">if</span> <span class="token punctuation">(</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>isFirstLoad<span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">var</span> onRegionChangeComplete <span class="token operator">=</span> <span class="token punctuation">(</span>region<span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
       <span class="token comment" spellcheck="true"> //When the MapView loads for the first time, we can create the annotation at the
</span>       <span class="token comment" spellcheck="true"> //region that was loaded.
</span>        <span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">setState<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
          isFirstLoad<span class="token punctuation">:</span> <span class="token boolean">false</span><span class="token punctuation">,</span>
          annotations<span class="token punctuation">:</span> <span class="token punctuation">[</span><span class="token keyword">this</span><span class="token punctuation">.</span><span class="token function">createAnnotation<span class="token punctuation">(</span></span>region<span class="token punctuation">.</span>longitude<span class="token punctuation">,</span> region<span class="token punctuation">.</span>latitude<span class="token punctuation">)</span><span class="token punctuation">]</span><span class="token punctuation">,</span>
        <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
      <span class="token punctuation">}</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>

    <span class="token keyword">return</span> <span class="token punctuation">(</span>
      &lt;MapView
        style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>map<span class="token punctuation">}</span>
        onRegionChangeComplete<span class="token operator">=</span><span class="token punctuation">{</span>onRegionChangeComplete<span class="token punctuation">}</span>
        region<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>mapRegion<span class="token punctuation">}</span>
        annotations<span class="token operator">=</span><span class="token punctuation">{</span><span class="token keyword">this</span><span class="token punctuation">.</span>state<span class="token punctuation">.</span>annotations<span class="token punctuation">}</span>
      <span class="token operator">/</span><span class="token operator">&gt;</span>
    <span class="token punctuation">)</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>

<span class="token keyword">var</span> styles <span class="token operator">=</span> StyleSheet<span class="token punctuation">.</span><span class="token function">create<span class="token punctuation">(</span></span><span class="token punctuation">{</span>
  map<span class="token punctuation">:</span> <span class="token punctuation">{</span>
    height<span class="token punctuation">:</span> <span class="token number">150</span><span class="token punctuation">,</span>
    margin<span class="token punctuation">:</span> <span class="token number">10</span><span class="token punctuation">,</span>
    borderWidth<span class="token punctuation">:</span> <span class="token number">1</span><span class="token punctuation">,</span>
    borderColor<span class="token punctuation">:</span> <span class="token string">'#000000'</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  row<span class="token punctuation">:</span> <span class="token punctuation">{</span>
    flexDirection<span class="token punctuation">:</span> <span class="token string">'row'</span><span class="token punctuation">,</span>
    justifyContent<span class="token punctuation">:</span> <span class="token string">'space-between'</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  textInput<span class="token punctuation">:</span> <span class="token punctuation">{</span>
    width<span class="token punctuation">:</span> <span class="token number">150</span><span class="token punctuation">,</span>
    height<span class="token punctuation">:</span> <span class="token number">20</span><span class="token punctuation">,</span>
    borderWidth<span class="token punctuation">:</span> <span class="token number">0.5</span><span class="token punctuation">,</span>
    borderColor<span class="token punctuation">:</span> <span class="token string">'#aaaaaa'</span><span class="token punctuation">,</span>
    fontSize<span class="token punctuation">:</span> <span class="token number">13</span><span class="token punctuation">,</span>
    padding<span class="token punctuation">:</span> <span class="token number">4</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  changeButton<span class="token punctuation">:</span> <span class="token punctuation">{</span>
    alignSelf<span class="token punctuation">:</span> <span class="token string">'center'</span><span class="token punctuation">,</span>
    marginTop<span class="token punctuation">:</span> <span class="token number">5</span><span class="token punctuation">,</span>
    padding<span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span>
    borderWidth<span class="token punctuation">:</span> <span class="token number">0.5</span><span class="token punctuation">,</span>
    borderColor<span class="token punctuation">:</span> <span class="token string">'#777777'</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

exports<span class="token punctuation">.</span>displayName <span class="token operator">=</span> <span class="token punctuation">(</span>undefined<span class="token punctuation">:</span> <span class="token operator">?</span>string<span class="token punctuation">)</span><span class="token punctuation">;</span>
exports<span class="token punctuation">.</span>title <span class="token operator">=</span> <span class="token string">'&lt;MapView&gt;'</span><span class="token punctuation">;</span>
exports<span class="token punctuation">.</span>description <span class="token operator">=</span> <span class="token string">'Base component to display maps'</span><span class="token punctuation">;</span>
exports<span class="token punctuation">.</span>examples <span class="token operator">=</span> <span class="token punctuation">[</span>
  <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Map'</span><span class="token punctuation">,</span>
    <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> &lt;MapViewExample <span class="token operator">/</span><span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'showsUserLocation + followUserLocation'</span><span class="token punctuation">,</span>
    <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> <span class="token punctuation">(</span>
        &lt;MapView
          style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>map<span class="token punctuation">}</span>
          showsUserLocation<span class="token operator">=</span><span class="token punctuation">{</span><span class="token boolean">true</span><span class="token punctuation">}</span>
          followUserLocation<span class="token operator">=</span><span class="token punctuation">{</span><span class="token boolean">true</span><span class="token punctuation">}</span>
        <span class="token operator">/</span><span class="token operator">&gt;</span>
      <span class="token punctuation">)</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Callout example'</span><span class="token punctuation">,</span>
    <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> &lt;AnnotationExample style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>map<span class="token punctuation">}</span> annotation<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>
        title<span class="token punctuation">:</span> <span class="token string">'More Info...'</span><span class="token punctuation">,</span>
        rightCalloutView<span class="token punctuation">:</span> <span class="token punctuation">(</span>
          &lt;TouchableOpacity
            onPress<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
              <span class="token function">alert<span class="token punctuation">(</span></span><span class="token string">'You Are Here'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
            <span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
            &lt;Image
              style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>width<span class="token punctuation">:</span><span class="token number">30</span><span class="token punctuation">,</span> height<span class="token punctuation">:</span><span class="token number">30</span><span class="token punctuation">}</span><span class="token punctuation">}</span>
              source<span class="token operator">=</span><span class="token punctuation">{</span><span class="token function">require<span class="token punctuation">(</span></span><span class="token string">'./uie_thumb_selected.png'</span><span class="token punctuation">)</span><span class="token punctuation">}</span>
            <span class="token operator">/</span><span class="token operator">&gt;</span>
          &lt;<span class="token operator">/</span>TouchableOpacity<span class="token operator">&gt;</span>
        <span class="token punctuation">)</span><span class="token punctuation">,</span>
      <span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">/</span><span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Show callouts by default example'</span><span class="token punctuation">,</span>
    <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> &lt;AnnotationExample
        style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>map<span class="token punctuation">}</span>
        annotation<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>
          title<span class="token punctuation">:</span> <span class="token string">'More Info...'</span><span class="token punctuation">,</span>
          rightCalloutView<span class="token punctuation">:</span> <span class="token punctuation">(</span>
            &lt;TouchableOpacity
              onPress<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
                <span class="token function">alert<span class="token punctuation">(</span></span><span class="token string">'You Are Here'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
              <span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
              &lt;Image
                style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>width<span class="token punctuation">:</span><span class="token number">30</span><span class="token punctuation">,</span> height<span class="token punctuation">:</span><span class="token number">30</span><span class="token punctuation">}</span><span class="token punctuation">}</span>
                source<span class="token operator">=</span><span class="token punctuation">{</span><span class="token function">require<span class="token punctuation">(</span></span><span class="token string">'./uie_thumb_selected.png'</span><span class="token punctuation">)</span><span class="token punctuation">}</span>
              <span class="token operator">/</span><span class="token operator">&gt;</span>
            &lt;<span class="token operator">/</span>TouchableOpacity<span class="token operator">&gt;</span>
          <span class="token punctuation">)</span><span class="token punctuation">,</span>
        <span class="token punctuation">}</span><span class="token punctuation">}</span>
        showsAnnotationCallouts<span class="token operator">=</span><span class="token punctuation">{</span><span class="token boolean">true</span><span class="token punctuation">}</span>
      <span class="token operator">/</span><span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Annotation focus example'</span><span class="token punctuation">,</span>
    <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> &lt;AnnotationExample style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>map<span class="token punctuation">}</span> annotation<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>
        title<span class="token punctuation">:</span> <span class="token string">'More Info...'</span><span class="token punctuation">,</span>
        onFocus<span class="token punctuation">:</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
          <span class="token function">alert<span class="token punctuation">(</span></span><span class="token string">'Annotation gets focus'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span><span class="token punctuation">,</span>
        onBlur<span class="token punctuation">:</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token punctuation">{</span>
          <span class="token function">alert<span class="token punctuation">(</span></span><span class="token string">'Annotation lost focus'</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
        <span class="token punctuation">}</span>
      <span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">/</span><span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Draggable pin'</span><span class="token punctuation">,</span>
    <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> &lt;DraggableAnnotationExample<span class="token operator">/</span><span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Custom pin color'</span><span class="token punctuation">,</span>
    <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> &lt;AnnotationExample style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>map<span class="token punctuation">}</span> annotation<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>
        title<span class="token punctuation">:</span> <span class="token string">'You Are Purple'</span><span class="token punctuation">,</span>
        tintColor<span class="token punctuation">:</span> MapView<span class="token punctuation">.</span>PinColors<span class="token punctuation">.</span>PURPLE<span class="token punctuation">,</span>
      <span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">/</span><span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Custom pin image'</span><span class="token punctuation">,</span>
    <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> &lt;AnnotationExample style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>map<span class="token punctuation">}</span> annotation<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>
        title<span class="token punctuation">:</span> <span class="token string">'Thumbs Up!'</span><span class="token punctuation">,</span>
        image<span class="token punctuation">:</span> <span class="token function">require<span class="token punctuation">(</span></span><span class="token string">'./uie_thumb_big.png'</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
      <span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">/</span><span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Custom pin view'</span><span class="token punctuation">,</span>
    <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> &lt;AnnotationExample style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>map<span class="token punctuation">}</span> annotation<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>
        title<span class="token punctuation">:</span> <span class="token string">'Thumbs Up!'</span><span class="token punctuation">,</span>
        view<span class="token punctuation">:</span> &lt;View style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>
          alignItems<span class="token punctuation">:</span> <span class="token string">'center'</span><span class="token punctuation">,</span>
        <span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
          &lt;Text style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>fontWeight<span class="token punctuation">:</span> <span class="token string">'bold'</span><span class="token punctuation">,</span> color<span class="token punctuation">:</span> <span class="token string">'#f007'</span><span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">&gt;</span>
            Thumbs Up<span class="token operator">!</span>
          &lt;<span class="token operator">/</span>Text<span class="token operator">&gt;</span>
          &lt;Image
            style<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>width<span class="token punctuation">:</span> <span class="token number">90</span><span class="token punctuation">,</span> height<span class="token punctuation">:</span> <span class="token number">65</span><span class="token punctuation">,</span> resizeMode<span class="token punctuation">:</span> <span class="token string">'cover'</span><span class="token punctuation">}</span><span class="token punctuation">}</span>
            source<span class="token operator">=</span><span class="token punctuation">{</span><span class="token function">require<span class="token punctuation">(</span></span><span class="token string">'./uie_thumb_big.png'</span><span class="token punctuation">)</span><span class="token punctuation">}</span>
          <span class="token operator">/</span><span class="token operator">&gt;</span>
        &lt;<span class="token operator">/</span>View<span class="token operator">&gt;</span><span class="token punctuation">,</span>
      <span class="token punctuation">}</span><span class="token punctuation">}</span><span class="token operator">/</span><span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">{</span>
    title<span class="token punctuation">:</span> <span class="token string">'Custom overlay'</span><span class="token punctuation">,</span>
    <span class="token function">render<span class="token punctuation">(</span></span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
      <span class="token keyword">return</span> &lt;MapView
        style<span class="token operator">=</span><span class="token punctuation">{</span>styles<span class="token punctuation">.</span>map<span class="token punctuation">}</span>
        region<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">{</span>
          latitude<span class="token punctuation">:</span> <span class="token number">39.06</span><span class="token punctuation">,</span>
          longitude<span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">95.22</span><span class="token punctuation">,</span>
        <span class="token punctuation">}</span><span class="token punctuation">}</span>
        overlays<span class="token operator">=</span><span class="token punctuation">{</span><span class="token punctuation">[</span><span class="token punctuation">{</span>
          coordinates<span class="token punctuation">:</span><span class="token punctuation">[</span>
            <span class="token punctuation">{</span>latitude<span class="token punctuation">:</span> <span class="token number">32.47</span><span class="token punctuation">,</span> longitude<span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">107.85</span><span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>latitude<span class="token punctuation">:</span> <span class="token number">45.13</span><span class="token punctuation">,</span> longitude<span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">94.48</span><span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>latitude<span class="token punctuation">:</span> <span class="token number">39.27</span><span class="token punctuation">,</span> longitude<span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">83.25</span><span class="token punctuation">}</span><span class="token punctuation">,</span>
            <span class="token punctuation">{</span>latitude<span class="token punctuation">:</span> <span class="token number">32.47</span><span class="token punctuation">,</span> longitude<span class="token punctuation">:</span> <span class="token operator">-</span><span class="token number">107.85</span><span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token punctuation">]</span><span class="token punctuation">,</span>
          strokeColor<span class="token punctuation">:</span> <span class="token string">'#f007'</span><span class="token punctuation">,</span>
          lineWidth<span class="token punctuation">:</span> <span class="token number">3</span><span class="token punctuation">,</span>
        <span class="token punctuation">}</span><span class="token punctuation">]</span><span class="token punctuation">}</span>
      <span class="token operator">/</span><span class="token operator">&gt;</span><span class="token punctuation">;</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
<span class="token punctuation">]</span><span class="token punctuation">;</span></div><div class="embedded-simulator"><p><a class="modal-button-open"><strong>Run this example</strong></a></p><div class="modal-button-open modal-button-open-img"><img alt="Run example in simulator" width="170" height="356" src="img/uiexplorer_main_ios.png"></div><div><div class="modal"><div class="modal-content"><button class="modal-button-close">×</button><div class="center"><iframe class="simulator" src="https://appetize.io/embed/7vdfm9h3e6vuf4gfdm7r5rgc48?device=iphone6s&amp;scale=60&amp;autoplay=false&amp;orientation=portrait&amp;deviceColor=white&amp;params=%7B%22route%22%3A%22MapView%22%7D" width="256" height="550" scrolling="no"></iframe><p>Powered by <a target="_blank" href="https://appetize.io">appetize.io</a></p></div></div></div><div class="modal-backdrop"></div></div></div></div></div></div><div class="docs-prevnext"><a class="docs-prev" href="docs/listview.html#content">← Prev</a><a class="docs-next" href="docs/modal.html#content">Next →</a></div>