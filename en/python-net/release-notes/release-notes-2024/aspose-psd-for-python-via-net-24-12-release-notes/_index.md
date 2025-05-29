---
title: Aspose.PSD for Python via .NET 24.12 - Release Notes
type: docs
weight: 10
url: /python-net/aspose-psd-for-python-via-net-24-12-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD for Python via .NET 24.12](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**     | **Summary**                                                                                                | **Category** |
|:--------------|:-----------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-143 | [AI Format] Rework Compound Paths to work through APS                                                      | Enhancement  |
| PSDPYTHON-137 | Implement correct handling of PSD file with Shape layer and having vector and raster masks                 | Feature      |
| PSDPYTHON-139 | [AI Format] Implement Gradient Shading (type 7)                                                            | Feature      |
| PSDPYTHON-141 | [AI Format] Implement blending support                                                                     | Feature      |
| PSDPYTHON-145 | [AI Format] Add AiImage property for number of pages                                                       | Feature      |
| PSDPYTHON-142 | [AI Format] Implement Axial Shading (type 2)                                                               | Feature      |
| PSDPYTHON-136 | Fix rendering of Shapes in PSD files created in an old version of the PS                                   | Bug          |
| PSDPYTHON-144 | [AI Format] Incorrect rendering of AI file                                                                 | Bug          |
| PSDPYTHON-146 | The GlobalResources property is null when PSD Image is just created that leads to errors with SmartObjects | Bug          |
| PSDPYTHON-147 | [Ai Format] Add handling of Layers data defined as DictionaryObject in Properties object of the Page       | Bug          |

## **Public API Changes**

# **Added APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResource.#ctor(System.Int32,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor(System.Int32,System.Byte[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AdjustmentLayerResource.#ctor(System.Int32,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BooleanResource.#ctor(System.Int32,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BooleanResource.#ctor(System.Int32,System.Byte[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.#ctor(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource.#ctor(System.Int32,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Ai.AiImage.PageCount

# **Removed APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BaseArtboardInfoResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LyvrResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CmlsResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CmlsResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CmlsResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AdjustmentLayerResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AdjustmentLayerResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BooleanResource.#ctor(System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BooleanResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BooleanResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BooleanResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BritResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BritResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CgEdResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CgEdResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IopaResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IopaResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IopaResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CustResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CustResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CustResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ExpaResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ExpaResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FxrpResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FxrpResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FxrpResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Hue2Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Hue2Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LclrResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LclrResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LclrResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.KnkoResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.InfxResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LayerSectionResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LayerSectionResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LayerSectionResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LevlResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LevlResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MixrResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MixrResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PhflResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PhflResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PhflResourceVersion2.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PhflResourceVersion2.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PhflResourceVersion3.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PhflResourceVersion3.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ShmdResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ShmdResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ShmdResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnsrResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnsrResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnsrResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LspfResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LspfResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LspfResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LuniResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LuniResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LuniResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClblResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LyidResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LyidResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LyidResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfo6Resource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfo6Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfo6Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.UnknownResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.UnknownResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CurvResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlwhResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.SetPsdVersion(System.UInt16)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.PsdVersion

## **Usage examples:**


**PSDPYTHON-143. [AI Format] Rework Compound Paths to work through APS**
{{< highlight python >}}
        source_file = self.GetFileInBaseFolder("page-3.ai")
        output_file = self.GetFileInOutputFolder("page-3.png")

        with AiImage.load(source_file) as img:
            image = cast(AiImage, img)
            image.save(output_file, PngOptions())
{{< /highlight >}}

**PSDPYTHON-137. Implement correct handling of PSD file with Shape layer and having vector and raster masks**
{{< highlight python >}}
        input_file = self.GetFileInBaseFolder("mask_rastr_vector.psd")
        output_file = self.GetFileInOutputFolder("output_mask_rastr_vector.png")

        with PsdImage.load(input_file, None) as img:
            image = cast(PsdImage, img)
            image.save(output_file, PngOptions())
{{< /highlight >}}

**PSDPYTHON-139. [AI Format] Implement Gradient Shading (type 7)**
{{< highlight python >}}
        source_file = self.GetFileInBaseFolder("2214.ai")
        output_file = self.GetFileInOutputFolder("2214.png")

        with AiImage.load(source_file) as img:
            image = cast(AiImage, img)
            image.save(output_file, PngOptions())
{{< /highlight >}}

**PSDPYTHON-141. [AI Format] Implement blending support**
{{< highlight python >}}
        source_file = self.GetFileInBaseFolder("2238.ai")
        output_file = self.GetFileInOutputFolder("2238.png")   

        with AiImage.load(source_file) as img:
            image = cast(AiImage, img)
            image.save(output_file, PngOptions())
{{< /highlight >}}

**PSDPYTHON-145. [AI Format] Add AiImage property for number of pages**
{{< highlight python >}}
		source_file = self.GetFileInBaseFolder("2241.ai")

        output_files = []
        for i in range(3):
            output_files.append(self.GetFileInOutputFolder(f"2241_pageNumber_{str(i)}.png"))

        with AiImage.load(source_file) as img:
            image = cast(AiImage, img)
            assert image.page_count == 3

            for i in range(image.page_count):
                image.active_page_index = i
                image.save(output_files[i], PngOptions())
{{< /highlight >}}

**PSDPYTHON-142. [AI Format] Implement Axial Shading (type 2)**
{{< highlight python >}}
        source_file = self.GetFileInBaseFolder("2249.ai")
        output_file = self.GetFileInOutputFolder("2249.png")

        with AiImage.load(source_file) as img:
            image = cast(AiImage, img)
            image.save(output_file, PngOptions())
{{< /highlight >}}

**PSDPYTHON-136. Fix rendering of Shapes in PSD files created in an old version of the PS**
{{< highlight python >}}
        input_file_stroke = self.GetFileInBaseFolder("Shape_Stroke.psd")
        output_file_stroke = self.GetFileInOutputFolder("output_Shape_Stroke.png")

        input_file_effects = self.GetFileInBaseFolder("Shape_Effects_PS2021.psd")
        output_file_effects = self.GetFileInOutputFolder("output_Shape_Effects_PS2021.png")

        # Test that there is no cropping of outside part of stroke in old psd format files.
        with PsdImage.load(input_file_stroke) as img:
            image = cast(PsdImage, img)
            for layer in image.layers:
                if  is_assignable(layer, ShapeLayer):
                    # Shape layer is repainted in this test
                    shape_layer = cast(ShapeLayer, layer)
                    shape_layer.update()

            image.save(output_file_stroke, PngOptions())

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True
        # Test effects rendering on Shape layers.
        with PsdImage.load(input_file_effects, opt) as img:
            image = cast(PsdImage, img)
            # Shape layer is not repainted in this test
            image.save(output_file_effects, PngOptions())
{{< /highlight >}}

**PSDPYTHON-144. [AI Format] Incorrect rendering of AI file**
{{< highlight python >}}
        source_file = self.GetFileInBaseFolder("Input1.ai")
        output_file = self.GetFileInOutputFolder("Input1.png")

        with AiImage.load(source_file) as img:
            image = cast(AiImage, img)
            image.save(output_file, PngOptions())
{{< /highlight >}}

**PSDPYTHON-146. The GlobalResources property is null when PSD Image is just created that leads to errors with SmartObjects**
{{< highlight python >}}
        with PsdImage(300, 100) as psdImage:
            assert hasattr(psdImage, 'global_layer_resources')
            assert psdImage.global_layer_resources is not None
{{< /highlight >}}

**PSDPYTHON-147. [Ai Format] Add handling of Layers data defined as DictionaryObject in Properties object of the Page**
{{< highlight python >}}       
        source_file = self.GetFileInBaseFolder("Input_2.ai")
        output_file = self.GetFileInOutputFolder("output.png")

        with AiImage.load(source_file) as img:
            image = cast(AiImage, img)
            image.save(output_file, PngOptions())
{{< /highlight >}}