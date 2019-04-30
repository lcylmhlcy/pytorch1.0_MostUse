# torchvision

## [torchvision.datasets](https://pytorch.org/docs/stable/torchvision/datasets.html)

- torchvision.datasets.MNIST(root, train=True, transform=None, target_transform=None, download=False)
- torchvision.datasets.FashionMNIST(root, train=True, transform=None, target_transform=None, download=False)
- torchvision.datasets.KMNIST(root, train=True, transform=None, target_transform=None, download=False)
- torchvision.datasets.EMNIST(root, split)
- torchvision.datasets.FakeData(size=1000, image_size=(3, 224, 224), num_classes=10, transform=None, target_transform=None, random_offset=0)
- torchvision.datasets.CocoCaptions(root, annFile, transform=None, target_transform=None)
- torchvision.datasets.CocoDetection(root, annFile, transform=None, target_transform=None)
- torchvision.datasets.LSUN(root, classes='train', transform=None, target_transform=None)
- torchvision.datasets.CIFAR10(root, train=True, transform=None, target_transform=None, download=False)
- torchvision.datasets.CIFAR100(root, train=True, transform=None, target_transform=None, download=False)
- torchvision.datasets.STL10(root, split='train', transform=None, target_transform=None, download=False)
- torchvision.datasets.SVHN(root, split='train', transform=None, target_transform=None, download=False)
- torchvision.datasets.PhotoTour(root, name, train=True, transform=None, download=False)
- torchvision.datasets.SBU(root, transform=None, target_transform=None, download=True)
- torchvision.datasets.Flickr8k(root, ann_file, transform=None, target_transform=None)
- torchvision.datasets.Flickr30k(root, ann_file, transform=None, target_transform=None)
- torchvision.datasets.VOCSegmentation(root, year='2012', image_set='train', download=False, transform=None, target_transform=None)
- torchvision.datasets.VOCDetection(root, year='2012', image_set='train', download=False, transform=None, target_transform=None)
- torchvision.datasets.Cityscapes(root, split='train', mode='fine', target_type='instance', transform=None, target_transform=None)
- torchvision.datasets.ImageFolder(root, transform=None, target_transform=None, loader=<function default_loader>)
- torchvision.datasets.DatasetFolder(root, loader, extensions, transform=None, target_transform=None)
- [Imagenet-12](https://github.com/facebook/fb.resnet.torch/blob/master/INSTALL.md#download-the-imagenet-dataset): use ImageFolder

## [torchvision.models](https://pytorch.org/docs/stable/torchvision/models.html)

- torchvision.models.alexnet(pretrained=False)
- torchvision.models.vgg11(pretrained=False)
- torchvision.models.vgg11_bn(pretrained=False)
- torchvision.models.vgg13(pretrained=False)
- torchvision.models.vgg13_bn(pretrained=False)
- torchvision.models.vgg16(pretrained=False)
- torchvision.models.vgg16_bn(pretrained=False)
- torchvision.models.vgg19(pretrained=False)
- torchvision.models.vgg19_bn(pretrained=False)
- torchvision.models.resnet18(pretrained=False)
- torchvision.models.resnet34(pretrained=False)
- torchvision.models.resnet50(pretrained=False)
- torchvision.models.resnet101(pretrained=False)
- torchvision.models.resnet152(pretrained=False)
- torchvision.models.squeezenet1_0(pretrained=False)
- torchvision.models.squeezenet1_1(pretrained=False)
- torchvision.models.densenet121(pretrained=False)
- torchvision.models.densenet169(pretrained=False)
- torchvision.models.densenet161(pretrained=False)
- torchvision.models.densenet201(pretrained=False)
- torchvision.models.inception_v3(pretrained=False)
- torchvision.models.googlenet(pretrained=False)

## [torchvision.transforms](https://pytorch.org/docs/stable/torchvision/transforms.html)

torchvision.transforms.Compose(transforms)

### Transforms on PIL Image

- torchvision.transforms.CenterCrop(size)
- torchvision.transforms.ColorJitter(brightness=0, contrast=0, saturation=0, hue=0)
- torchvision.transforms.FiveCrop(size)
- torchvision.transforms.Grayscale(num_output_channels=1)
- torchvision.transforms.Pad(padding, fill=0, padding_mode='constant')
- torchvision.transforms.RandomAffine(degrees, translate=None, scale=None, shear=None, resample=False, fillcolor=0)
- torchvision.transforms.RandomApply(transforms, p=0.5)
- torchvision.transforms.RandomChoice(transforms)
- torchvision.transforms.RandomCrop(size, padding=None, pad_if_needed=False, fill=0, padding_mode='constant'
- torchvision.transforms.RandomGrayscale(p=0.1)
- torchvision.transforms.RandomHorizontalFlip(p=0.5)
- torchvision.transforms.RandomOrder(transforms)
- torchvision.transforms.RandomResizedCrop(size, scale=(0.08, 1.0), ratio=(0.75, 1.3333333333333333), interpolation=2)
- torchvision.transforms.RandomRotation(degrees, resample=False, expand=False, center=None)
- torchvision.transforms.RandomSizedCrop()
- torchvision.transforms.RandomVerticalFlip(p=0.5)
- torchvision.transforms.Resize(size, interpolation=2)
- torchvision.transforms.Scale()
- torchvision.transforms.TenCrop(size, vertical_flip=False)

### Transforms on torch.Tensor

- torchvision.transforms.LinearTransformation(transformation_matrix)
- torchvision.transforms.Normalize(mean, std, inplace=False)

### Conversion Transforms

- torchvision.transforms.ToPILImage(mode=None)
- torchvision.transforms.ToTensor

### Generic Transforms

- torchvision.transforms.Lambda(lambd)

### Functional Transforms

Functional transforms give you fine-grained control of the transformation pipeline. As opposed to the transformations above, functional transforms don’t contain a random number generator for their parameters. That means you have to specify/generate all parameters, but you can reuse the functional transform. For example, you can apply a functional transform to multiple images like this:

- torchvision.transforms.functional.adjust_brightness(img, brightness_factor)
- torchvision.transforms.functional.adjust_contrast(img, contrast_factor)
- torchvision.transforms.functional.adjust_gamma(img, gamma, gain=1)
- torchvision.transforms.functional.adjust_hue(img, hue_factor)
- torchvision.transforms.functional.adjust_saturation(img, saturation_factor)
- torchvision.transforms.functional.affine(img, angle, translate, scale, shear, resample=0, fillcolor=None)
- torchvision.transforms.functional.crop(img, i, j, h, w)
- torchvision.transforms.functional.five_crop(img, size)
- torchvision.transforms.functional.hflip(img)
- torchvision.transforms.functional.normalize(tensor, mean, std, inplace=False)
- torchvision.transforms.functional.pad(img, padding, fill=0, padding_mode='constant')
- torchvision.transforms.functional.resize(img, size, interpolation=2)
- torchvision.transforms.functional.resized_crop(img, i, j, h, w, size, interpolation=2)
- torchvision.transforms.functional.rotate(img, angle, resample=False, expand=False, center=None)
- torchvision.transforms.functional.ten_crop(img, size, vertical_flip=False)
- torchvision.transforms.functional.to_grayscale(img, num_output_channels=1)
- torchvision.transforms.functional.to_pil_image(pic, mode=None)
- torchvision.transforms.functional.to_tensor(pic)
- torchvision.transforms.functional.vflip(img)

## [torchvision.utils](https://pytorch.org/docs/stable/torchvision/utils.html)

- torchvision.utils.make_grid(tensor, nrow=8, padding=2, normalize=False, range=None, scale_each=False, pad_value=0)
- torchvision.utils.save_image(tensor, filename, nrow=8, padding=2, normalize=False, range=None, scale_each=False, pad_value=0)