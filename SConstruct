
file = 'pf'

import os
import threading
import time
from multiprocessing import Process, Lock

env = Environment(ENV=os.environ)
env.PDF(target = file + '.pdf', source = file + '.tex')
os.system('open -a Preview ' + file + '.pdf')


#pdfCreated = threading.Event()
#finished = threading.Event()
#
#def check_pid(pid):        
#    """ Check For the existence of a unix pid. """
#    try:
#        os.kill(pid, 0)
#    except OSError:
#        return False
#    else:
#        return True
#
#env.PDF(target = file + '.pdf', source = file + '.tex')
#
#def run_1():
#  while 1:
#    if os.path.isfile(file+'.pdf'):
#      os.system('rm ' + file + '.pdf')
#    if os.path.isfile(file+'.glo'):
#      os.system('rm ' + file + '.glo')
#    env.PDF(target = file + '.pdf', source = file + '.tex')
#    pdfCreated.wait()
#    print '------------------- Action 1 ------------------------------'
#
#
#def watch_pdf():
#  oldsize = 0.
#  while 1:
#    if not os.path.isfile(file+'.pdf'):
#      pass
#    else:
#      print '--------------------- Found pdf --------------------------'
#      newsize = os.path.getsize(file)
#      if newsize == oldsize:
#        print newsize, oldsize
#        pdfCreated.set()
#        break
#      else:
#        oldsize = newsize
#  
#
#def run_2():
#  print 'run_2'
#  while 1:
#    print '---------------------- Waiting Action 2 -------------------------'
#    pdfCreated.wait()
#    print '---------------------- Action 2 ---------------------------'
#    os.system('makeglossaries ' + file + '.glo')
#    break
#
#
#def run_3():
#  while 1:
#    if not os.path.isfile(file+'.glo'):
#      pass
#    else:
#      print '----------------------- Action 3 -----------------------------'
#      os.system('pdflatex ' + file + '.tex')
#      os.system('open -a Preview ' + file + '.pdf')
#      finished.set()
#      break
#
#threadPdf = threading.Thread(target=watch_pdf, args=())
#threadPdf.setDaemon(True)
#threadPdf.start()
#print 'Here', threading.enumerate()
#
#thread1 = threading.Thread(target=run_1, args=())
#thread1.setDaemon(True)
#thread1.start()
#thread1.join()
#print 'Here', threading.enumerate()
#
#
#
#thread2 = threading.Thread(target=run_2, args=())
#thread2.setDaemon(True)
#thread2.start()
#time.sleep(1)
#print 'Here', threading.enumerate()
#
#
#thread3 = threading.Thread(target=run_3, args=())
#thread3.setDaemon(True)
#thread3.start()
#print 'Here', threading.enumerate()
#
#print 'Waiting finished'
##finished.wait()
#print 'Finished'
#
#thread2.join()
#thread3.join()
#
