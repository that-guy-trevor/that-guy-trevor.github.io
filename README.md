<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <title>Recursive Backtracking - Permute</title>
    <link rel="stylesheet" type="text/css" href="./normalize.min.css">
    <link rel="stylesheet" type="text/css" href="./style.css">
  </head>
  <body>
    <div class="container">
      <div class="top-row">
        <div class="button-container">
          <div class="button normal" id="button-prev">Prev</div>
          <div class="button normal" id="button-next">Next</div>
          <div class="button wide" id="button-run">Play</div>
          <div class="button wide" id="button-stop">Stop</div>
          <div class="button wide" id="debug-case">&nbsp;</div>
        </div>
        <div class="code-editor-container">
          <div id="editor-overlay" class="editor-overlay">
            <div id="e-o-row" class="row">&nbsp;</div>
          </div>
          <div class="code-editor">
            <div class="line-nums-sidebar">
              <div class="line-num">1</div>
              <div class="line-num">2</div>
              <div class="line-num">3</div>
              <div class="line-num">4</div>
              <div class="line-num">5</div>
              <div class="line-num">6</div>
              <div class="line-num">7</div>
              <div class="line-num">8</div>
              <div class="line-num">9</div>
              <div class="line-num">10</div>
              <div class="line-num">11</div>
              <div class="line-num">12</div>
              <div class="line-num">13</div>
              <div class="line-num">14</div>
              <div class="line-num">15</div>
              <div class="line-num">16</div>
              <div class="line-num">17</div>
              <div class="line-num">18</div>
              <div class="line-num">19</div>
              <div class="line-num">20</div>
              <div class="line-num">21</div>
              <div class="line-num">22</div>
              <div class="line-num">23</div>
              <div class="line-num">24</div>
              <div class="line-num">25</div>
              <div class="line-num">26</div>
              <div class="line-num">27</div>
              <div class="line-num">28</div>
              <div class="line-num">29</div>
              <div class="line-num">30</div>
            </div>
            <div class="code">
              <div class="line-of-code">
                <c-c># Get all permutations of an array</c-c>
              </div>
              <div class="line-of-code">
                <c-r>def</c-r>
                <c-g>permute</c-g>(nums: <c-b>list</c-b>[<c-b>int</c-b>]) <c-r>-></c-r>
                <c-b>list</c-b>[<c-b>list</c-b>[<c-b>int</c-b>]]:
              </div>
              <div class="line-of-code">
                <tab-1>n, sol, ans <c-r>=</c-r>
                  <c-b>len</c-b>(nums), [], []
                </tab-1>
              </div>
              <div class="line-of-code">
                <tab-1>
                  <c-r>def</c-r>
                  <c-g>backtrack</c-g>():
                </tab-1>
              </div>
              <div class="line-of-code">
                <tab-2>
                  <c-r>if </c-r>n <c-r>==</c-r>
                  <c-b>len</c-b>(sol):
                </tab-2>
              </div>
              <div class="line-of-code">
                <tab-3>ans.<c-b>append</c-b>(sol[:]) </tab-3>
              </div>
              <div class="line-of-code">
                <tab-3>
                  <c-r>return</c-r>
                </tab-3>
              </div>
              <div class="line-of-code">
                <tab-2>
                  <c-r>for</c-r> x <c-r>in </c-r>nums:
                </tab-2>
              </div>
              <div class="line-of-code">
                <tab-3>
                  <c-r>if</c-r> x <c-r>not in</c-r> sol:
                </tab-3>
              </div>
              <div class="line-of-code">
                <tab-4>sol.<c-b>append</c-b>(x) </tab-4>
              </div>
              <div class="line-of-code">
                <tab-4>backtrack()</tab-4>
              </div>
              <div class="line-of-code">
                <tab-4>sol.<c-b>pop</c-b>() </tab-4>
              </div>
              <div class="line-of-code">
                <tab-2>
                  <c-r>return</c-r>
              </div>
              <div class="line-of-code">
                <tab-1>backtrack()</tab-1>
              </div>
              <div class="line-of-code">
                <tab-1>
                  <c-r>return</c-r> ans
                </tab-1>
              </div>
              <div class="line-of-code">&nbsp;</div>
              <div class="line-of-code">permute([<c-p>1</c-p>, <c-p>2</c-p>, <c-p>3</c-p>])</div>
            </div>
          </div>
        </div>
        <div class="call-stack-container">
          <div class="rotated-text">
            <div>Call Stack</div>
          </div>
          <div class="call-stack-bucket" id="call-stack-bucket">&nbsp;</div>
        </div>
        <div class="vars">
          <div class="header">Variables</div>
          <div class="item">
            <div class="label">n</div>
            <div class="value">
              <c-p>3</c-p>
            </div>
          </div>
          <div class="item">
            <div class="label">sol</div>
            <div class="value" id="sol-values">
              <div id="lb-sol-item">[</div>
              <div id="add-to-sol"></div>
              <div id="rb-sol-item">]</div>
            </div>
          </div>
          <div class="item">
            <div class="label">ans</div>
            <div class="value">[ <div style="opacity:0" id="ans-index-0">[ <c-p>1</c-p>, <c-p>2</c-p>, <c-p>3</c-p>], </div>
              <div style="opacity:0" id="ans-index-1">[ <c-p>1</c-p>, <c-p>3</c-p>, <c-p>2</c-p>], </div>
              <div style="opacity:0" id="ans-index-2">[ <c-p>2</c-p>, <c-p>1</c-p>, <c-p>3</c-p>], </div>
              <div style="opacity:0" id="ans-index-3">[ <c-p>2</c-p>, <c-p>3</c-p>, <c-p>1</c-p>], </div>
              <div style="opacity:0" id="ans-index-4">[ <c-p>3</c-p>, <c-p>1</c-p>, <c-p>2</c-p>], </div>
              <div style="opacity:0" id="ans-index-5">[ <c-p>3</c-p>, <c-p>2</c-p>, <c-p>1</c-p>] </div>
              <div id="rb-ans-item" style="position:relative;vertical-align:top;top:-129px;left:7px">]</div>
            </div>
          </div>
        </div>
      </div>
      <div class="bottom-row" id="bottom-row"></div>
    </div>
    <script src="./gsap.min.js" type="text/javascript" charset="utf-8"></script>
    <script src="./tsparticles.confetti.bundle.min.js" type="text/javascript" charset="utf-8"></script>
    <script src="./script.min.js" type="text/javascript" charset="utf-8"></script>
  </body>
</html>
