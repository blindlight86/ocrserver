# ocrserver

The minimum OCR server by Golang

# start

```sh
sudo apt-get install -y libleptonica-dev libtesseract-dev tesseract-ocr
go get github.com/otiai10/ocrserver
$GOPATH/bin/ocrserver
```

# endpoints

`GET /status`

```sh
% curl -XGET "http://localhost:9900/status"
{"message":"Hello!","version":"0.0.1-default"}

```

`POST /base64`

```sh
% curl -XPOST "http://localhost:9900/base64" -d '{"base64":"iVBORw0KGgoAAAANSUhEUgAAACEAAAAOCAYAAAChHnWMAAACtElEQVQ4T82VPUhyYRTH/7eSorbIaiilxVWLhhwKiaRB3EQQijbzI9uiDxz8IISiQs2MshYxCNoaAxebgoYMclEiQigqqqUoUl/OgWteTV54l7ezPc99Pn7P/3/OuUKpVCrhP4fw6yBubm6wu7uLh4cH1qazsxMmkwlqtVqi1ePjI/b395HL5Xi+o6MDVqsVSqWSx3d3dzg+PpbsEQQBKpUKg4ODaG1tlX4TlTg9PUU8HgctNpvNvJDGX19fGBgYwPT0NG9Mp9OIRCJoaGjA5OQkmpqacHBwgPf3d9jtdmg0GmSzWayurqK3t5fPo3h7ewPBNzc3Y2NjA42NjWUQtoMucjqd6O7uhtfrlVDSYXSo2+1GT08PHA4HXxwOhyXrZmZmGHh7e7sMEY1GGVaMl5cXzM/PIxAIoL29XQpxeHiIZDJZ85FWFYtFfuHo6CjGxsawtLQEn8+Hrq4uCcT9/T2ur68xNDRUF+Lj4wOzs7NYXl5mC8VgJUKhEPsbDAZ/rBOCIL/1ej12dnawubkJmUxWt6ZEO9bW1spKkAqkMtlAKtbYsbKygnw+/1eI8fFxlntra0tySDWNCPETZX9/P2w2W21ikhKZTKaccNWbKSlHRkbYEo/H86MSVFnr6+v8EBGCYMWcoHYUi8Vwfn4Ouo8SVGLH1dUVb7ZYLNDpdBKGk5MTHB0dYW5uDgqFAi6XiyuALKqMxcVFvL6+skoiRHViPj8/Y2Fhge9qaWmRQtCIsr5QKHBfIO8pUqkUEokE5HI5/H4/z+3t7eHs7AxarRZTU1M8R5ddXFyUH1EPQkxMUqytra0WggCodG5vbyUv7OvrY/rKoMS8vLz8PkQQYDAYYDQaea4exOfnJys5PDyMiYmJWghxhpoONRUK6piV3lWC0Kuenp5AXlO5Uu/41/gV/44/SvNv5iv8RRoAAAAASUVORK5CYII=", "trim":"\n"}'
{
	"result": "OCR"
}
```