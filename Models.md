# MODELS/ class MnemonicScheme(models.Model):
### **`CharField`**

Используется для хранения строк текста фиксированной длины.

- **`max_length`**: `int` — максимальная длина строки (обязательный параметр).
- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`choices`**: `list of tuples` — позволяет выбрать значение из ограниченного набора (опционально).
- **`default`**: `various` — значение по умолчанию (опционально).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`TextField`**

Используется для хранения больших объемов текста.

- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`default`**: `various` — значение по умолчанию (опционально).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`IntegerField`**

Используется для хранения целых чисел.

- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`default`**: `int` — значение по умолчанию (опционально).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`DecimalField`**

Используется для хранения десятичных чисел с фиксированной точностью.

- **`max_digits`**: `int` — общее количество цифр, включая десятичные (обязательный параметр).
- **`decimal_places`**: `int` — количество цифр после десятичной точки (обязательный параметр).
- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`default`**: `decimal.Decimal` — значение по умолчанию (опционально).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`FloatField`**

Используется для хранения чисел с плавающей запятой.

- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`default`**: `float` — значение по умолчанию (опционально).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`BooleanField`**

Используется для хранения значения `True` или `False`.

- **`default`**: `bool` — значение по умолчанию (опционально).
- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`DateField`**

Используется для хранения даты.

- **`auto_now`**: `bool` — устанавливает поле на текущее время при каждом сохранении (по умолчанию `False`).
- **`auto_now_add`**: `bool` — устанавливает поле на текущее время при создании (по умолчанию `False`).
- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`default`**: `datetime.date` — значение по умолчанию (опционально).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`DateTimeField`**

Используется для хранения даты и времени.

- **`auto_now`**: `bool` — устанавливает поле на текущее время при каждом сохранении (по умолчанию `False`).
- **`auto_now_add`**: `bool` — устанавливает поле на текущее время при создании (по умолчанию `False`).
- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`default`**: `datetime.datetime` — значение по умолчанию (опционально).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`TimeField`**

Используется для хранения времени (без даты).

- **`auto_now`**: `bool` — устанавливает поле на текущее время при каждом сохранении (по умолчанию `False`).
- **`auto_now_add`**: `bool` — устанавливает поле на текущее время при создании (по умолчанию `False`).
- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`default`**: `datetime.time` — значение по умолчанию (опционально).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`EmailField`**

Используется для хранения электронных адресов.

- **`max_length`**: `int` — максимальная длина строки (по умолчанию 254).
- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`default`**: `str` — значение по умолчанию (опционально).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`URLField`**

Используется для хранения URL.

- **`max_length`**: `int` — максимальная длина строки (по умолчанию 200).
- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`default`**: `str` — значение по умолчанию (опционально).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`ForeignKey`**

Используется для создания связи один ко многим.

- **`to`**: `Model` — модель, на которую ссылается внешний ключ (обязательный параметр).
- **`on_delete`**: `django.db.models.deletion` — поведение при удалении связанного объекта (обязательный параметр).
- **`related_name`**: `str` — имя обратной связи (опционально).
- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**: `bool` — позволяет ли поле быть `NULL` в базе данных (по умолчанию `False`).
- **`default`**: `Model` — значение по умолчанию (опционально).
- **`verbose_name`**: `str` — отображаемое имя поля (опционально).

### **`OneToOneField`**

Используется для создания связи один к одному.

- **`to`**: `Model` — модель, на которую ссылается одно из полей (обязательный параметр).
- **`on_delete`**: `django.db.models.deletion` — поведение при удалении связанного объекта (обязательный параметр).
- **`related_name`**: `str` — имя обратной связи (опционально).
- **`blank`**: `bool` — позволяет ли поле быть пустым в формах (по умолчанию `False`).
- **`null`**


```python
class ExampleModel(models.Model):
    title = models.CharField(max_length=255, verbose_name="Заголовок")
    slug = models.SlugField(max_length=255, unique=True, db_index=True, verbose_name="URL")
		photo = models.ImageField(upload_to='photos/%Y/%m/%d/', default=None,
                              blank=True, null=True, verbose_name='Фото')
		content = models.TextField(blank=True, verbose_name="Текст статьи")
		time_create = models.DateTimeField(auto_now_add=True, verbose_name="Время создания")
		file = models.FileField(upload_to='uploads_model')
    time_update = models.DateTimeField(auto_now=True)
    is_published = models.BooleanField(choices=Status.choices, default=Status.DRAFT, verbose_name="Статус")
    cat = models.ForeignKey('Category', on_delete=models.PROTECT, related_name='posts')
    tags = models.ManyToManyField('TagPost', blank=True, related_name='tags')
    husband = models.OneToOneField('Husband', on_delete=models.SET_NULL, null=True, blank=True, related_name='wuman',
                                   verbose_name="Муж")
    author = models.ForeignKey(get_user_model(), on_delete=models.SET_NULL, related_name='posts', null=True, default=None)

    objects = models.Manager()
    published = PublishedManager()

    def __str__(self):
        return self.title

    class Meta:
        verbose_name = 'Известные женщины'
        verbose_name_plural = 'Известные женщины'
        ordering = ['-time_create']
        indexes = [
            models.Index(fields=['-time_create'])
        ]

    def get_absolute_url(self):
        return reverse('post', kwargs={'post_slug': self.slug})

    def save(self, *args, **kwargs):
        self.slug = slugify(unidecode(str(self.title)))
        super().save(*args, **kwargs)
```
# FORMS/Поля форм Django

### **`CharField`**

Используется для ввода строкового текста.

- **`max_length`**: `int` — максимальная длина строки (обязательный параметр).
- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `various` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`EmailField`**

Используется для ввода электронного адреса.

- **`max_length`**: `int` — максимальная длина строки (по умолчанию 254).
- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `str` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`IntegerField`**

Используется для ввода целых чисел.

- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `int` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`DecimalField`**

Используется для ввода десятичных чисел.

- **`max_digits`**: `int` — общее количество цифр, включая десятичные (обязательный параметр).
- **`decimal_places`**: `int` — количество цифр после десятичной точки (обязательный параметр).
- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `decimal.Decimal` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`FloatField`**

Используется для ввода чисел с плавающей запятой.

- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `float` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`BooleanField`**

Используется для выбора значения `True` или `False`.

- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `bool` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`DateField`**

Используется для ввода даты.

- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `datetime.date` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`DateTimeField`**

Используется для ввода даты и времени.

- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `datetime.datetime` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`TimeField`**

Используется для ввода времени (без даты).

- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `datetime.time` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`URLField`**

Используется для ввода URL.

- **`max_length`**: `int` — максимальная длина строки (по умолчанию 200).
- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `str` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`ChoiceField`**

Используется для выбора из заданного набора опций.

- **`choices`**: `list of tuples` — список кортежей с вариантами выбора (обязательный параметр).
- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `various` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`MultipleChoiceField`**

Используется для выбора нескольких опций из набора.

- **`choices`**: `list of tuples` — список кортежей с вариантами выбора (обязательный параметр).
- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `list` — начальное значение (опционально).
- **`help_text`**: `str` — текст помощи, отображаемый рядом с полем (опционально).
- **`label`**: `str` — метка, отображаемая для поля (опционально).

### **`FileField`**

Используется для загрузки файлов.

- **`upload_to`**: `str` — путь, по которому будут загружаться файлы (опционально).
- **`required`**: `bool` — указывает, что поле обязательно для заполнения (по умолчанию `True`).
- **`widget`**: `Widget` — виджет, используемый для отображения поля (опционально).
- **`initial`**: `various` — начальное значение

```python
from captcha.fields import CaptchaField
from django import forms
from django.core.exceptions import ValidationError
from django.core.validators import MinLengthValidator, MaxLengthValidator

from .models import Category, Husband, Women


class AddPostForm(forms.ModelForm):
    # cat = forms.ModelChoiceField(queryset=Category.objects.all(), empty_label='Категория не выбрана', required=False,
    #                              label='Категории')
    # husband = forms.ModelChoiceField(queryset=Husband.objects.all(), empty_label='Муж не выбран', label='Муж')

    class Meta:
        model = Women
        fields = ['title', 'slug', 'photo', 'content', 'is_published', 'cat', 'husband', 'tags']
        widgets = {
            'title': forms.TextInput(attrs={'class': 'form-input'}),
            'content': forms.Textarea(attrs={'rows': 5, 'cols': 50}),
        }
        labels = {'slug': 'URL'}

    def clean_title(self):
        title = self.cleaned_data['title']
        if len(title) > 50:
            raise ValidationError('Длина превышает 50 символов')

        return title


class UploadFileForm(forms.Form):
    file = forms.FileField(label='Файл')


class ContactForm(forms.Form):
    name = forms.CharField(label='Имя', max_length=255)
    email = forms.EmailField(label='Email')
    content = forms.CharField(widget=forms.Textarea(attrs={'cols': 60, 'rows': 10}))
    captcha = CaptchaField()
```